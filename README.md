Programacion2
=============


import java.awt.*;
import javax.swing.*;
import java.awt.Event;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;




public class Programacion2 extends JFrame


    
     {
	
	   private final JLabel nombre = new JLabel ("Primer Nombre");
	   private final JLabel apellido = new JLabel ("Primer Apellido");    
	   
	   private final JTextField campo_nombre = new JTextField (25);
	   private final JTextField campo_apellido = new JTextField (25);    
	
	   
	   private final JButton aceptar = new JButton ("Buscar");
	   private final JButton cancelar = new JButton ("Vaciar");
	   private final JButton saludo = new JButton ("Inf.Del Sistema");

	   public  Programacion2 ()
	   
	   
	   {
		  	   
		  setTitle( "Bienvenido" );
		  setSize( 500 , 250 );
		  setLocation( 250 , 250 );
		  setResizable( true );
		 
	
		  Container contenedor = getContentPane();
		  SpringLayout Layout = new SpringLayout();
          contenedor.setLayout ( Layout );	 
          
          aceptar.addActionListener(new ActionListener()
    
          {
        	public void actionPerformed( ActionEvent Evento ) 
        	{
        		
        		if( campo_nombre.getText().isEmpty() || campo_apellido.getText().isEmpty())
        			
        		{
        			
        			JOptionPane.showMessageDialog( getContentPane(), "Debe llenar los campos de texto", "Error" , JOptionPane.ERROR_MESSAGE);
        		}
        		
        		else {
        			JOptionPane.showMessageDialog( getContentPane(),"Tu Usuario ha sido buscado Correctamente" , "Listo" , JOptionPane.PLAIN_MESSAGE);
        		}
        	}
          });
          
          saludo.addActionListener(new ActionListener()
          
          {
        	public void actionPerformed( ActionEvent Evento ) 
        	{
        		
        		if( campo_nombre.getText().isEmpty() || campo_apellido.getText().isEmpty())
        			
        		{
        			
        			JOptionPane.showMessageDialog( getContentPane(), "Debe llenar los campos de texto", "Error" , JOptionPane.ERROR_MESSAGE);
        		}
        		
        		else {
        			JOptionPane.showMessageDialog( getContentPane(),"Ud. No Esta Registrado Gracias por Preferirnos "+"Sr(a) " + campo_nombre.getText() +" "  +  campo_apellido.getText() , "Bienvenido" , JOptionPane.PLAIN_MESSAGE);
        		}
        	}
          });
          
          
          
          cancelar.addActionListener(new ActionListener()
          
          {
        	public void actionPerformed( ActionEvent Evento ) 
        	{
        		
        		if( campo_nombre.getText().isEmpty() || !campo_apellido.getText().isEmpty())
        			
        		{
        			
        			JOptionPane.showMessageDialog( getContentPane(), "Los Campos se encuentran Limpios", "Exito" , JOptionPane.PLAIN_MESSAGE);
        		
        			campo_nombre.setText(" ");
        			campo_apellido.setText(" ");
        	
        		}
        		
        		else {
        			JOptionPane.showMessageDialog( getContentPane(),"Ya los campos estan listo para usarse", "Reintentar" , JOptionPane.ERROR_MESSAGE);
        		}
        	}
          });
          
          Layout.putConstraint (SpringLayout.WEST, nombre,40, SpringLayout.WEST,contenedor);
          Layout.putConstraint (SpringLayout.NORTH, nombre,40, SpringLayout.NORTH,contenedor);
	   

          Layout.putConstraint (SpringLayout.WEST, campo_nombre,150, SpringLayout.WEST,contenedor);
          Layout.putConstraint (SpringLayout.NORTH, campo_nombre,40, SpringLayout.NORTH,contenedor);
	     
          Layout.putConstraint (SpringLayout.WEST, apellido,50, SpringLayout.WEST,contenedor);
          Layout.putConstraint (SpringLayout.NORTH, apellido,100, SpringLayout.NORTH,contenedor);
          
          Layout.putConstraint (SpringLayout.WEST, campo_apellido,150, SpringLayout.WEST,contenedor);
          Layout.putConstraint (SpringLayout.NORTH, campo_apellido,100, SpringLayout.NORTH,contenedor);
	     
          Layout.putConstraint (SpringLayout.WEST, aceptar,50, SpringLayout.WEST,contenedor);
          Layout.putConstraint (SpringLayout.NORTH, aceptar,180, SpringLayout.NORTH,contenedor);
          
          Layout.putConstraint (SpringLayout.WEST, cancelar,350, SpringLayout.WEST,contenedor);
          Layout.putConstraint (SpringLayout.NORTH, cancelar,180, SpringLayout.NORTH,contenedor);
          
          Layout.putConstraint (SpringLayout.WEST, saludo,165, SpringLayout.WEST,contenedor);
          Layout.putConstraint (SpringLayout.NORTH, saludo,180, SpringLayout.NORTH,contenedor);
         
	   contenedor.add (nombre);
	   contenedor.add (campo_nombre);
	   contenedor.add (apellido);
	   contenedor.add (campo_apellido);
	   contenedor.add (aceptar);
	   contenedor.add (cancelar);
	   contenedor.add (saludo);
	   setVisible(true);
	   
	   
     } 
	   
	    public static void main(String[] arguments) {

	    	Programacion2 iniciar = new Programacion2 ();
			iniciar.setVisible (true );
	        
	    
	    }
}
    
