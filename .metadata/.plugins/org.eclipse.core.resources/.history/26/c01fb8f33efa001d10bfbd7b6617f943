package imcArrayList;

import java.util.ArrayList;

import javax.swing.JOptionPane;

public class Procesos {
	
	ArrayList<Double> peso = new ArrayList<Double>();
	
	ArrayList<Double> talla = new ArrayList<Double>();
	
	ArrayList<String> nombres = new ArrayList<String>();
	
	double operacion;
	
	int pregunta;

	
	public void iniciar() {
		System.out.println("Inicio");
		String menu="GESTION IMC\n";
		menu+="1. Llenar Datos\n";
		menu+="2. Imprimir Datos\n";
		menu+="3. Imprimir IMC\n";
		menu+="4. Buscar por nombre\n";
		menu+="5. Eliminar todo\n";
		menu+="6. Actualizar\n";
		menu+="7. Salir\n";
		menu+="Ingrese una opcion:\n";

		int opc=0;
		do {
			opc=Integer.parseInt(JOptionPane.showInputDialog(menu));
			validarMenu(opc);
			
		} while (opc!=7);
		
		
	}
	
	
	private void validarMenu(int opc) {
		switch (opc) {
		case 1:
			pedirDatos();
			 	break;
		case 2:
			if(validarArreglo()) {
			imprimirDatos();
			}
		 		break;
		case 3:
			if(validarArreglo()) {
				procesoDatos();
			}
			break;
		case 4:

			if(validarArreglo()) {
				buscarnombre();
			}
			break;
		case 5:
			if(validarArreglo()) {
				borrarDatos();
			}
			break;
		case 7:
			System.out.println("Chao!");
		 	break;
		default:
			System.out.println("Ingrese una opcion valida");
			break;
		}
}
	

	private void procesoDatos() {
		for(int i = 0; i < nombres.size(); i += 1) {
			
			operacion = peso.get(i) / (talla.get(i)*talla.get(i));
			
			if(operacion < 18) {
				System.out.println("Hola "+nombres.get(i)+" Segun su peso su estado es ANOREXIA");
			}else if(operacion >= 18 && operacion < 20) {
				System.out.println("Hola "+nombres.get(i)+" Segun su peso su estado es DELGADEZ");
			}else if(operacion >= 20 && operacion < 27) {
				System.out.println("Hola "+nombres.get(i)+" Segun su peso su estado es NORMAL");
			}else if(operacion > 27 && operacion < 30) {
				System.out.println("Hola "+nombres.get(i)+" Segun su peso su estado es OBESIDAD 1");
			}else if(operacion >=30 && operacion < 35) {
				System.out.println("Hola "+nombres.get(i)+" Segun su peso su estado es OBESIDAD 2");
			}else if(operacion >= 35 && operacion < 40) {
				System.out.println("Hola "+nombres.get(i)+" Segun su peso su estado es OBESIDAD 3");
			}else if(operacion >= 40) {
				System.out.println("Hola "+nombres.get(i)+" Segun su peso su estado es OBESIDAD 4");
			}
			
		}
	}
	
	
	
	public boolean validarArreglo() {
		if (nombres!=null) {
			return true;
		}else {
			System.out.println("Debe primero llenar datos");
			return false;
		}
	}
	
	
	private void pedirDatos() {

		nombres.add(JOptionPane.showInputDialog("Ingrese su nombre"));
		peso.add(Double.parseDouble(JOptionPane.showInputDialog("Ingrese su peso")));
		talla.add(Double.parseDouble(JOptionPane.showInputDialog("Ingrese su altura")));
		
	}
	
	
	public void imprimirDatos() {
		System.out.println("Las lista de usuarios es: ");
		for (int i = 0; i < nombres.size(); i+=1) {
			System.out.println(nombres.get(i));
		}
		
	}
	
	
	public void buscarnombre() {
        int contador = 0;

        String nombrebuscar = JOptionPane.showInputDialog("ingrese el nombre a buscar");

        for (int i = 0; i < nombres.size(); i+=1) {
            if (nombres.get(i).equalsIgnoreCase(nombrebuscar)) {
                System.out.println("se encontro a "+nombrebuscar+" en la posicion "+(i+1));
                contador+=1;
            }
        }

        if (contador>0) {
            System.out.println("Encontro a "+nombrebuscar+" "+contador+" veces");
        }else{
            System.out.println("la persona "+nombrebuscar+" no fue registrada");
        }

    }
	
	
	public void borrarDatos() {
	 
	        nombres.clear();
	        talla.clear();
	        peso.clear();
	        
	    }
	}