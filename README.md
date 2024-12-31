in order to set up the code you need to download java and its IDE.
after that write this code

package pos.system;

import java.text.DecimalFormat;
import java.util.Vector;
import javax.swing.table.DefaultTableModel;

/**
 *
 * @author andre
 */
public class POSSystem1 extends javax.swing.JFrame {

    /**
     * Creates new form POSSystem1
     */
    public POSSystem1() {
        initComponents();
        
        Table1.getColumnModel().getColumn(0).setPreferredWidth(30);
        Table1.getColumnModel().getColumn(1).setPreferredWidth(200);


    }

   public void addtable(int ID ,String Name, int Qty, Double Price){
      
      DefaultTableModel dt = (DefaultTableModel) Table1.getModel();
       
       DecimalFormat df = new DecimalFormat("00.00");
       double TedPrice =Price * Double.valueOf(Qty);
       String TotalPrice = df.format(TedPrice);
      
      //product allready add chk
      
       for (int row = 0; row < Table1.getRowCount(); row++) {
           if (Name == Table1.getValueAt(row, 1)){
           dt.removeRow(Table1.convertRowIndexToModel(row));
          
           }          
       }
      
      
      
       Vector v = new Vector();
       
        v.add(ID);
        v.add(Name);
        v.add(Qty);
        v.add(TotalPrice);

        dt.addRow(v);
    }
   
   public void cal(){
   //cal total table values
   
   int numberofRow = Table1.getRowCount();
   double Ted = 0.0;
   
       for (int i = 0; i < numberofRow; i++) {
           
           double worth = Double.valueOf(Table1.getValueAt(i, 3).toString());
           Ted += worth ;
        
       }
       DecimalFormat df = new DecimalFormat("00.00");
       Total.setText(df.format(Ted));
       
   
   }
    
    
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jPanel1 = new javax.swing.JPanel();
        jPanel2 = new javax.swing.JPanel();
        Combo1 = new javax.swing.JButton();
        Combo2 = new javax.swing.JButton();
        Combo3 = new javax.swing.JButton();
        T1 = new javax.swing.JLabel();
        T2 = new javax.swing.JLabel();
        T3 = new javax.swing.JLabel();
        jPanel3 = new javax.swing.JPanel();
        Combo4 = new javax.swing.JButton();
        BucketCombo = new javax.swing.JButton();
        ChickenFilletBurger = new javax.swing.JButton();
        T5 = new javax.swing.JLabel();
        T6 = new javax.swing.JLabel();
        T4 = new javax.swing.JLabel();
        ChickenBurger = new javax.swing.JButton();
        Combo6 = new javax.swing.JButton();
        Combo7 = new javax.swing.JButton();
        T7 = new javax.swing.JLabel();
        T8 = new javax.swing.JLabel();
        T9 = new javax.swing.JLabel();
        jPanel4 = new javax.swing.JPanel();
        jScrollPane2 = new javax.swing.JScrollPane();
        Table1 = new javax.swing.JTable();
        jScrollPane1 = new javax.swing.JScrollPane();
        Bill = new javax.swing.JTextArea();
        jPanel5 = new javax.swing.JPanel();
        Remain = new javax.swing.JLabel();
        Total1 = new javax.swing.JLabel();
        Total = new javax.swing.JLabel();
        Cash = new javax.swing.JLabel();
        Balance = new javax.swing.JLabel();
        Print = new javax.swing.JButton();
        Pay = new javax.swing.JButton();
        Delete = new javax.swing.JButton();
        Payment = new javax.swing.JTextField();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        Combo1.setIcon(new javax.swing.ImageIcon("C:\\Users\\andre\\OneDrive\\Pictures\\1.jpg")); // NOI18N
        Combo1.setText("jButton2");
        Combo1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                Combo1ActionPerformed(evt);
            }
        });

        Combo2.setIcon(new javax.swing.ImageIcon("C:\\Users\\andre\\OneDrive\\Pictures\\2.jpg")); // NOI18N
        Combo2.setText("jButton1");
        Combo2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                Combo2ActionPerformed(evt);
            }
        });

        Combo3.setIcon(new javax.swing.ImageIcon("C:\\Users\\andre\\OneDrive\\Pictures\\3.jpg")); // NOI18N
        Combo3.setText("jButton1");
        Combo3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                Combo3ActionPerformed(evt);
            }
        });

        T1.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        T1.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        T1.setText("0");

        T2.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        T2.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        T2.setText("0");

        T3.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        T3.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        T3.setText("0");

        Combo4.setIcon(new javax.swing.ImageIcon("C:\\Users\\andre\\OneDrive\\Pictures\\4.jpg")); // NOI18N
        Combo4.setText("jButton2");
        Combo4.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                Combo4ActionPerformed(evt);
            }
        });

        BucketCombo.setIcon(new javax.swing.ImageIcon("C:\\Users\\andre\\OneDrive\\Pictures\\5.jpg")); // NOI18N
        BucketCombo.setText("jButton1");
        BucketCombo.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                BucketComboActionPerformed(evt);
            }
        });

        ChickenFilletBurger.setIcon(new javax.swing.ImageIcon("C:\\Users\\andre\\OneDrive\\Pictures\\6.jpg")); // NOI18N
        ChickenFilletBurger.setText("jButton1");
        ChickenFilletBurger.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                ChickenFilletBurgerActionPerformed(evt);
            }
        });

        T5.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        T5.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        T5.setText("0");

        T6.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        T6.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        T6.setText("0");

        T4.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        T4.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        T4.setText("0");

        javax.swing.GroupLayout jPanel3Layout = new javax.swing.GroupLayout(jPanel3);
        jPanel3.setLayout(jPanel3Layout);
        jPanel3Layout.setHorizontalGroup(
            jPanel3Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel3Layout.createSequentialGroup()
                .addGroup(jPanel3Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(Combo4, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addGroup(jPanel3Layout.createSequentialGroup()
                        .addContainerGap()
                        .addComponent(T4, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(jPanel3Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                    .addComponent(T5, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(BucketCombo, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(jPanel3Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(ChickenFilletBurger, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(T6, javax.swing.GroupLayout.Alignment.TRAILING, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE)))
        );
        jPanel3Layout.setVerticalGroup(
            jPanel3Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, jPanel3Layout.createSequentialGroup()
                .addGroup(jPanel3Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(BucketCombo, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(Combo4, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(ChickenFilletBurger, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(jPanel3Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(T5, javax.swing.GroupLayout.PREFERRED_SIZE, 26, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(T6, javax.swing.GroupLayout.PREFERRED_SIZE, 26, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(T4, javax.swing.GroupLayout.PREFERRED_SIZE, 26, javax.swing.GroupLayout.PREFERRED_SIZE)))
        );

        ChickenBurger.setIcon(new javax.swing.ImageIcon("C:\\Users\\andre\\OneDrive\\Pictures\\7.jpg")); // NOI18N
        ChickenBurger.setText("jButton2");
        ChickenBurger.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                ChickenBurgerActionPerformed(evt);
            }
        });

        Combo6.setIcon(new javax.swing.ImageIcon("C:\\Users\\andre\\OneDrive\\Pictures\\8.jpg")); // NOI18N
        Combo6.setText("jButton2");
        Combo6.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                Combo6ActionPerformed(evt);
            }
        });

        Combo7.setIcon(new javax.swing.ImageIcon("C:\\Users\\andre\\OneDrive\\Pictures\\10.jpg")); // NOI18N
        Combo7.setText("jButton2");
        Combo7.setToolTipText("");
        Combo7.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                Combo7ActionPerformed(evt);
            }
        });

        T7.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        T7.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        T7.setText("0");

        T8.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        T8.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        T8.setText("0");

        T9.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        T9.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        T9.setText("0");

        javax.swing.GroupLayout jPanel2Layout = new javax.swing.GroupLayout(jPanel2);
        jPanel2.setLayout(jPanel2Layout);
        jPanel2Layout.setHorizontalGroup(
            jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel2Layout.createSequentialGroup()
                .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(jPanel2Layout.createSequentialGroup()
                        .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING, false)
                            .addComponent(T1, javax.swing.GroupLayout.Alignment.LEADING, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                            .addComponent(Combo1, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                            .addComponent(T2, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                            .addComponent(Combo2, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addComponent(Combo3, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addComponent(T3, javax.swing.GroupLayout.Alignment.TRAILING, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE)))
                    .addGroup(jPanel2Layout.createSequentialGroup()
                        .addContainerGap()
                        .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addComponent(jPanel3, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addGroup(jPanel2Layout.createSequentialGroup()
                                .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                                    .addGroup(javax.swing.GroupLayout.Alignment.LEADING, jPanel2Layout.createSequentialGroup()
                                        .addComponent(T7, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                        .addComponent(T8, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                                    .addGroup(javax.swing.GroupLayout.Alignment.LEADING, jPanel2Layout.createSequentialGroup()
                                        .addComponent(ChickenBurger, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE)
                                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                        .addComponent(Combo6, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE)))
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                                    .addComponent(Combo7, javax.swing.GroupLayout.PREFERRED_SIZE, 121, javax.swing.GroupLayout.PREFERRED_SIZE)
                                    .addComponent(T9, javax.swing.GroupLayout.Alignment.TRAILING, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))))))
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
        );
        jPanel2Layout.setVerticalGroup(
            jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, jPanel2Layout.createSequentialGroup()
                .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(Combo2, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(Combo1, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(Combo3, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(T2, javax.swing.GroupLayout.PREFERRED_SIZE, 26, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                        .addComponent(T1, javax.swing.GroupLayout.PREFERRED_SIZE, 26, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addComponent(T3, javax.swing.GroupLayout.PREFERRED_SIZE, 26, javax.swing.GroupLayout.PREFERRED_SIZE)))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jPanel3, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(ChickenBurger, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(Combo6, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(Combo7, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addGap(1, 1, 1)
                .addGroup(jPanel2Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(T7, javax.swing.GroupLayout.PREFERRED_SIZE, 26, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(T8, javax.swing.GroupLayout.PREFERRED_SIZE, 26, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(T9, javax.swing.GroupLayout.PREFERRED_SIZE, 26, javax.swing.GroupLayout.PREFERRED_SIZE)))
        );

        Table1.setFont(new java.awt.Font("Segoe UI", 1, 14)); // NOI18N
        Table1.setModel(new javax.swing.table.DefaultTableModel(
            new Object [][] {

            },
            new String [] {
                "ID", "Item", "Qty", "Price"
            }
        ));
        Table1.addAncestorListener(new javax.swing.event.AncestorListener() {
            public void ancestorAdded(javax.swing.event.AncestorEvent evt) {
                Table1AncestorAdded(evt);
            }
            public void ancestorMoved(javax.swing.event.AncestorEvent evt) {
            }
            public void ancestorRemoved(javax.swing.event.AncestorEvent evt) {
            }
        });
        jScrollPane2.setViewportView(Table1);

        Bill.setColumns(20);
        Bill.setFont(new java.awt.Font("Segoe UI", 1, 12)); // NOI18N
        Bill.setRows(5);
        jScrollPane1.setViewportView(Bill);

        Remain.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        Remain.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        Remain.setText("Balance:");

        Total1.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        Total1.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        Total1.setText("Total:");

        Total.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        Total.setText("00");

        Cash.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        Cash.setHorizontalAlignment(javax.swing.SwingConstants.CENTER);
        Cash.setText("Cash:");

        Balance.setFont(new java.awt.Font("Segoe UI", 1, 18)); // NOI18N
        Balance.setText("00");

        Print.setFont(new java.awt.Font("Segoe UI", 1, 24)); // NOI18N
        Print.setText("Print");
        Print.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                PrintActionPerformed(evt);
            }
        });

        Pay.setFont(new java.awt.Font("Segoe UI", 1, 24)); // NOI18N
        Pay.setText("Pay");
        Pay.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                PayActionPerformed(evt);
            }
        });

        Delete.setFont(new java.awt.Font("Segoe UI", 1, 24)); // NOI18N
        Delete.setText("Delete");
        Delete.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                DeleteActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout jPanel5Layout = new javax.swing.GroupLayout(jPanel5);
        jPanel5.setLayout(jPanel5Layout);
        jPanel5Layout.setHorizontalGroup(
            jPanel5Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel5Layout.createSequentialGroup()
                .addGroup(jPanel5Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                    .addGroup(jPanel5Layout.createSequentialGroup()
                        .addContainerGap()
                        .addComponent(Remain, javax.swing.GroupLayout.PREFERRED_SIZE, 79, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(Balance, javax.swing.GroupLayout.PREFERRED_SIZE, 148, javax.swing.GroupLayout.PREFERRED_SIZE))
                    .addGroup(jPanel5Layout.createSequentialGroup()
                        .addGroup(jPanel5Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                            .addComponent(Total1, javax.swing.GroupLayout.PREFERRED_SIZE, 79, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addGroup(javax.swing.GroupLayout.Alignment.LEADING, jPanel5Layout.createSequentialGroup()
                                .addContainerGap()
                                .addComponent(Cash, javax.swing.GroupLayout.PREFERRED_SIZE, 76, javax.swing.GroupLayout.PREFERRED_SIZE)))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addGroup(jPanel5Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                            .addComponent(Total, javax.swing.GroupLayout.DEFAULT_SIZE, 148, Short.MAX_VALUE)
                            .addComponent(Payment))))
                .addGap(18, 18, 18)
                .addComponent(Pay, javax.swing.GroupLayout.PREFERRED_SIZE, 96, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(18, 18, 18)
                .addComponent(Print, javax.swing.GroupLayout.PREFERRED_SIZE, 96, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(18, 18, 18)
                .addComponent(Delete)
                .addGap(0, 121, Short.MAX_VALUE))
        );
        jPanel5Layout.setVerticalGroup(
            jPanel5Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, jPanel5Layout.createSequentialGroup()
                .addContainerGap()
                .addGroup(jPanel5Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                    .addGroup(jPanel5Layout.createSequentialGroup()
                        .addGroup(jPanel5Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                            .addComponent(Total1, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                            .addComponent(Total, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addGroup(jPanel5Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                            .addComponent(Cash, javax.swing.GroupLayout.DEFAULT_SIZE, 38, Short.MAX_VALUE)
                            .addComponent(Payment))
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addGroup(jPanel5Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                            .addComponent(Remain, javax.swing.GroupLayout.PREFERRED_SIZE, 32, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addComponent(Balance, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)))
                    .addComponent(Pay, javax.swing.GroupLayout.Alignment.LEADING, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                    .addComponent(Delete, javax.swing.GroupLayout.Alignment.LEADING, javax.swing.GroupLayout.DEFAULT_SIZE, 113, Short.MAX_VALUE)
                    .addComponent(Print, javax.swing.GroupLayout.Alignment.LEADING, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addGap(18, 18, 18))
        );

        javax.swing.GroupLayout jPanel4Layout = new javax.swing.GroupLayout(jPanel4);
        jPanel4.setLayout(jPanel4Layout);
        jPanel4Layout.setHorizontalGroup(
            jPanel4Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel4Layout.createSequentialGroup()
                .addGroup(jPanel4Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(jPanel4Layout.createSequentialGroup()
                        .addComponent(jScrollPane2, javax.swing.GroupLayout.PREFERRED_SIZE, 341, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(18, 18, 18)
                        .addComponent(jScrollPane1, javax.swing.GroupLayout.PREFERRED_SIZE, 335, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(0, 14, Short.MAX_VALUE))
                    .addComponent(jPanel5, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                .addContainerGap())
        );
        jPanel4Layout.setVerticalGroup(
            jPanel4Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel4Layout.createSequentialGroup()
                .addContainerGap()
                .addGroup(jPanel4Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                    .addComponent(jScrollPane2, javax.swing.GroupLayout.DEFAULT_SIZE, 372, Short.MAX_VALUE)
                    .addComponent(jScrollPane1))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jPanel5, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                .addContainerGap())
        );

        javax.swing.GroupLayout jPanel1Layout = new javax.swing.GroupLayout(jPanel1);
        jPanel1.setLayout(jPanel1Layout);
        jPanel1Layout.setHorizontalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addComponent(jPanel2, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addComponent(jPanel4, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addContainerGap())
        );
        jPanel1Layout.setVerticalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addComponent(jPanel2, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addComponent(jPanel4, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                .addContainerGap())
        );

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addComponent(jPanel1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(0, 0, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addComponent(jPanel1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(0, 0, Short.MAX_VALUE))
        );

        pack();
    }// </editor-fold>                        

    private void Combo4ActionPerformed(java.awt.event.ActionEvent evt) {                                       
         int i = Integer.valueOf(T4.getText());
        ++i;
        T4.setText(String.valueOf(i));
        
        addtable(1,"Combo4     ", i, 149.99);
        
        cal();
    }                                      

    private void ChickenBurgerActionPerformed(java.awt.event.ActionEvent evt) {                                              
        int i = Integer.valueOf(T7.getText());
        ++i;
        T7.setText(String.valueOf(i));
        
        addtable(1,"ChicBurger", i, 59.99);
        
        cal();
    }                                             

    private void Combo6ActionPerformed(java.awt.event.ActionEvent evt) {                                       
       int i = Integer.valueOf(T8.getText());
        ++i;
        T8.setText(String.valueOf(i));
        
        addtable(1,"Combo6   ", i, 119.99);
        
        cal();
    }                                      

    private void Combo7ActionPerformed(java.awt.event.ActionEvent evt) {                                       
        int i = Integer.valueOf(T8.getText());
        ++i;
        T8.setText(String.valueOf(i));
        
        addtable(1,"Combo7   ", i, 99.99);
        
        cal();
    }                                      

    private void Combo1ActionPerformed(java.awt.event.ActionEvent evt) {                                       
        // btn code
        int i = Integer.valueOf(T1.getText());
        ++i;
        T1.setText(String.valueOf(i));
        
        addtable(1,"Combo1   ", i, 79.99);
        
        cal();
    }                                      

    private void Table1AncestorAdded(javax.swing.event.AncestorEvent evt) {                                     
        // TODO add your handling code here:
    }                                    

    private void Combo2ActionPerformed(java.awt.event.ActionEvent evt) {                                       
       int i = Integer.valueOf(T2.getText());
        ++i;
        T2.setText(String.valueOf(i));
        
        addtable(1,"Combo2   ", i, 99.99);
        
        cal();
    }                                      

    private void Combo3ActionPerformed(java.awt.event.ActionEvent evt) {                                       
         int i = Integer.valueOf(T3.getText());
        ++i;
        T3.setText(String.valueOf(i));
        
        addtable(1,"Combo3      ", i, 129.99);
        
        cal();
    }                                      

    private void BucketComboActionPerformed(java.awt.event.ActionEvent evt) {                                            
  int i = Integer.valueOf(T5.getText());
        ++i;
        T5.setText(String.valueOf(i));
        
        addtable(1,"MIniBucket ", i, 549.99);
        
        cal();        cal();    }                                           

    private void ChickenFilletBurgerActionPerformed(java.awt.event.ActionEvent evt) {                                                    
  int i = Integer.valueOf(T6.getText());
        ++i;
        T6.setText(String.valueOf(i));
        
        addtable(1,"FilletBurger", i, 49.99);
        
        cal();    }                                                   

    private void PayActionPerformed(java.awt.event.ActionEvent evt) {                                    
        // Pay
      
        double Sum = Double.valueOf(Total.getText());
        double Cash = Double.valueOf(Payment.getText());
        double Remain = Cash - Sum;
        
          DecimalFormat df = new DecimalFormat("00.00");
     
       
        Balance.setText(String.valueOf(df.format(Remain)));
    }                                   

    private void DeleteActionPerformed(java.awt.event.ActionEvent evt) {                                       
         //Delete Item
         
         DefaultTableModel dt = (DefaultTableModel) Table1.getModel();
        
           String T = dt.getValueAt(Table1.getSelectedRow(), 0).toString();
         
           //Remove Product
         int TD = Table1.getSelectedRow();
         dt.removeRow(TD);
         
         //Remove Quality Label
         System.out.println(T);
         switch(T) {
          
             case "1":
                 T1.setText("0");
                 break;
             case "2":
                 T2.setText("0");
                 break;
             case "3":
                 T3.setText("0");
                 break;
             case "4":
                 T4.setText("0");
                 break;
             case "5":
                 T5.setText("0");
                 break;
             case "6":
                 T6.setText("0");
                 break;
             case "7":
                 T7.setText("0");
                 break;
             case "8":
                 T8.setText("0");
                 break;
             case "9":
                 T9.setText("0");
                 break;

                 default:
                 System.out.println("End");
         }
    }                                      

    private void PrintActionPerformed(java.awt.event.ActionEvent evt) {                                      
        // Recipe Print
        
        try {
        
            Bill.setText("                                    Grand Food \n");
            Bill.setText(Bill.getText() + "             SantaLucia,Digos City, Davao del Sur \n");
            Bill.setText(Bill.getText() + "             Mindanao< Philippines\n");
            Bill.setText(Bill.getText() + "             09064956983\n");
            Bill.setText(Bill.getText() + "---------------------------------------------------------------\n");
            Bill.setText(Bill.getText() + "  Item \t\tQty \tPrice" + "\n");
            Bill.setText(Bill.getText() + "---------------------------------------------------------------\n");

            DefaultTableModel dt = (DefaultTableModel) Table1.getModel();

            //get table detail
            for (int i = 0; i < Table1.getRowCount(); i++) {

                String ID = dt.getValueAt(i, 1).toString();
                String Qty = dt.getValueAt(i, 2).toString();
                String Price = dt.getValueAt(i, 3).toString();
                
                Bill.setText(Bill.getText() +"  "+ ID +"\t\t"+ Qty +"\t"+ Price + "\n");

            }            
             Bill.setText(Bill.getText() + "---------------------------------------------------------------\n");
             Bill.setText(Bill.getText() +"Sub Total: " + Total.getText() +"\n");
             Bill.setText(Bill.getText() +"Cash     : " + Payment.getText() +"\n");
             Bill.setText(Bill.getText() +"Balance: " + Balance.getText() +"\n");
             Bill.setText(Bill.getText() + "---------------------------------------------------------------\n");
             Bill.setText(Bill.getText() + "Thank You For you Purchase...!"+"\n");
             Bill.setText(Bill.getText() + "---------------------------------------------------------------\n");
             
        } catch (Exception e){
        
        }
    }                                     

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(POSSystem1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(POSSystem1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(POSSystem1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(POSSystem1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new POSSystem1().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JLabel Balance;
    private javax.swing.JTextArea Bill;
    private javax.swing.JButton BucketCombo;
    private javax.swing.JLabel Cash;
    private javax.swing.JButton ChickenBurger;
    private javax.swing.JButton ChickenFilletBurger;
    private javax.swing.JButton Combo1;
    private javax.swing.JButton Combo2;
    private javax.swing.JButton Combo3;
    private javax.swing.JButton Combo4;
    private javax.swing.JButton Combo6;
    private javax.swing.JButton Combo7;
    private javax.swing.JButton Delete;
    private javax.swing.JButton Pay;
    private javax.swing.JTextField Payment;
    private javax.swing.JButton Print;
    private javax.swing.JLabel Remain;
    private javax.swing.JLabel T1;
    private javax.swing.JLabel T2;
    private javax.swing.JLabel T3;
    private javax.swing.JLabel T4;
    private javax.swing.JLabel T5;
    private javax.swing.JLabel T6;
    private javax.swing.JLabel T7;
    private javax.swing.JLabel T8;
    private javax.swing.JLabel T9;
    private javax.swing.JTable Table1;
    private javax.swing.JLabel Total;
    private javax.swing.JLabel Total1;
    private javax.swing.JPanel jPanel1;
    private javax.swing.JPanel jPanel2;
    private javax.swing.JPanel jPanel3;
    private javax.swing.JPanel jPanel4;
    private javax.swing.JPanel jPanel5;
    private javax.swing.JScrollPane jScrollPane1;
    private javax.swing.JScrollPane jScrollPane2;
    // End of variables declaration                   
}
then you can proceed on running it either you press contrl then f6 or you can rught click then click run.
