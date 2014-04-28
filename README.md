mirepositorio
=============
public class Hilos extends Thread{

String mensaje;

 public Hilos (String nota){
	 
	 
	 
	 super (nota);
	 
 }
 
 public void run(){
	 
	 
	 for (int i=0; i<10; i++){
		 System.out.println(mensaje);
	 }
	 System.out.println("este proceso ha finalizado:"+this.getName());
 }
public void setMensaje (String nota){
	this.mensaje = nota ;
}
	
	
	
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub

		Hilos hilo1 = new Hilos ("hilo a");
		Hilos hilo2 = new Hilos ("hilo b");
		hilo1.setMensaje("mensaje del hilo a");
		hilo2.setMensaje("mensaje del hilo b");

		hilo1.start();
		hilo2.start();
		hilo1.getName();
		hilo2.getName();

		

	}

}
