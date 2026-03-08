// List<Usuario> lista = gestor.listar();
                                // for (Usuario usuario : lista) {
                                //     System.out.println(usuario);
                                // }
                                // System.out.println();
                                // List<Libros> lista2 = gestor.listarLibros();
                                // for (Libros libro : lista2) {
                                //     System.out.println(libro);
                                // }
                                // System.out.println();
                                gestor.listarLibrosOrdenadosPorAño();
                                List<Libros> lista3 = gestor.listarLibros();
                                for (Libros u: lista3) {
                                    System.out.print("Titulo: " + u.getTitulo() + " | " + "Autor: " + u.getAutor() + " | " + "Año: " + u.getAño() + "| " + "Stock: " + u.getStock());
                                    System.out.println();
                                }


                                
                                System.out.print("Digite el nombre del usuario: ");
                                String nombre = sc.nextLine();
                                
                                System.out.print("Digite el email del usuario: ");
                                String email = sc.nextLine();
                                
                                System.out.print("Digite la ciudad de nacimiento del usuario: ");
                                String ciudad = sc.nextLine();
                                
                                int nuevoId = gestor.obtenerSiguienteId();
                                boolean exito = gestor.crear(new Usuario(nuevoId, nombre, email, ciudad));
                                
                                if (exito) {
                                    System.out.println("¡Cliente creado con éxito! Se le asignó el ID: " + nuevoId);
                                }
                                break;
