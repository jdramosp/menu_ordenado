package progra;

import java.util.Random;
import java.util.Scanner;


public class Progra {
    public static void main(String[] args) {
        // TODO code application logic here
        
        Scanner sn = new Scanner(System.in);
        
        boolean salir = false;
        
        int opcion; 
        
        ArrayFunciones a = new ArrayFunciones();
        
        do{
           System.out.println("1 llenar arreglo aleatoriamente");
           System.out.println("2 ordenar arreglo ascendente");
           System.out.println("3 ordenar descendente");
           System.out.println("4 Salir");
           
           System.out.println("Escribe una de las opciones");
           
           opcion = sn.nextInt();
           
           switch(opcion){
               case 1:
                   a.metodoAlet();            
                   break;
               case 2:
                   a.metodoAsce();
                   break;
                case 3:
                   a.metodoDesc();
                   break;
                case 4:
                    System.out.println("Salio de la aplicacion.");
                    salir=true;
                   break;
                default:
                   System.out.println("Solo números entre 1 y 4");
            }
       }while(!salir);
      }
    } 

//---------------------------------------------------------------------------//


package progra;

import java.util.ArrayList;
import java.util.Random;

/**
 *
 * @author Julio Ramos
 */
public class ArrayFunciones {
    
        ArrayList<Integer> al = new ArrayList<Integer>();
        ArrayList<Integer> al1 = new ArrayList<Integer>();
        ArrayList<Integer> al2 = new ArrayList<Integer>();
    
        public void metodoAsce( )//Función sin parámetros
        {
           
            int numeros = 0;
        
            while(numeros <= 100){
                
                al.add(numeros++);
                
            }
            
            System.out.print(al);
            
        }
        
    public void metodoAlet(){
        
        
      int min = 0;
      int max = 100;
      
      int numeros = 0;
      
      for(int i =0; i <=100; i++){
          int random_int = (int)Math.floor(Math.random()*(max-min+1)+min);
                
                al1.add(random_int);         
            }
       System.out.print(al1);
    }
    
    public void metodoDesc( )//Función sin parámetros
        {
           
            int numeros = 100;
        
            while(numeros >= 0){
                
                al2.add(numeros--);        
            }         
            System.out.print(al2);
            
        }
}
