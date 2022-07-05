# Meghna-Biswal
B-tech CSE,
//WAP java program to create a calculater using applet. 
import java.applet.*;
import java.awt.*;
import java.awt.event.*;
public class CalculaterDemo extends Applet implements ActionListener{
TextField tf1,tf2,tf3;
Button b1,b2,b3,b4;
Label l1,l2,l3;

public void init(){
setSize(300,150);
setVisible(true);
tf1=new TextField(120);
tf2=new TextField(120);
tf3=new TextField(120);

l1=new Label("Enter First Number");
l2=new Label("Enter second Number");
l3=new Label("Result");

b1=new Button("ADD");
b2=new Button("SUB");
b3=new Button("MUL");
b4=new Button("DIV");
//setLayout(new FlowLayout());
l1.setBounds( 20,50,130,20);
l2.setBounds( 20,80,130,20);
l3.setBounds( 20,110,130,20);

tf1.setBounds( 180,50,100,20);
tf2.setBounds( 180,80,100,20);
tf3.setBounds( 180,110,100,20);

b1.setBounds(20,160,100,30);
b2.setBounds(120,160,100,30);
b3.setBounds(220,160,100,30);
b4.setBounds(320,160,100,30);

setLayout(null);
add(l1);
add(tf1);

add(l2);
add(tf2);

add(l3);
add(tf3);

add(b1);
add(b2);
add(b3);
add(b4);

b1.addActionListener(this);
b2.addActionListener(this);
b3.addActionListener(this);
b4.addActionListener(this);
}
public void actionPerformed(ActionEvent ae){
int x= Integer.parseInt(tf1.getText());
int y= Integer.parseInt(tf2.getText());
if(ae.getSource()==b1){
int z=x+y;
tf3.setText(String.valueOf(z));
}
if(ae.getSource()==b2){
int z=x-y;
tf3.setText(String.valueOf(z));
}
if(ae.getSource()==b3){
int z=x*y;
tf3.setText(String.valueOf(z));
}
if(ae.getSource()==b4){
int z=x/y;
tf3.setText(String.valueOf(z));
}


}
}
/*
 *<applet code=CalculaterDemo.class width=600 height=600>
 *</applet>
 */
