# Menu
//Menu simple de opciones
 
        System.out.println("Digite una opcion");

        Scanner sn = new Scanner(System.in);
        boolean salir = false;
        int opcion;
        while (!salir) {
            System.out.println("1. Registrar Cliente");
            System.out.println("2. Opcion 2");
            System.out.println("3. Opcion 3");
            System.out.println("4. Salir");

            try {

                System.out.println("Escribe una de las opciones");
                opcion = sn.nextInt();

                switch (opcion) {
                    case 1:
                        System.out.println("Ingrese datos del cliente");
                        Scanner cli=new Scanner(System.in);

                        String registro;
                        registro= cli.nextLine();
                        String rut;
                        rut= cli.nextLine();
                        Cliente c1=new Cliente();
                        c1.setNombre(registro);
                        c1.setRut(rut);
                        System.out.println("Cliente: "+c1);
                        break;
                    case 2:
                        System.out.println("Has seleccionado la opcion 2");
                        break;
                    case 3:
                        System.out.println("Has seleccionado la opcion 3");
                        break;
                    case 4:
                        salir = true;
                        break;
                    default:
                        System.out.println("Solo números entre 1 y 4");
                }
            } catch (InputMismatchException e) {
                System.out.println("Debes insertar un número");
                sn.next();
            }
        }
