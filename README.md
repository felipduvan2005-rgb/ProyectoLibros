# ProyectoLibros
public class Libro {
    private String titulo;
    private String autor;
    private int numEjemplares;
    private int numPrestados;

    public Libro() {
        this.titulo = "";
        this.autor = "";
        this.numEjemplares = 0;
        this.numPrestados = 0;
    }

    public Libro(String titulo, String autor, int numEjemplares, int numPrestados) {
        this.titulo = titulo;
        this.autor = autor;
        this.numEjemplares = numEjemplares;
        this.numPrestados = numPrestados;
    }

    public String getTitulo() { return titulo; }
    public void setTitulo(String titulo) { this.titulo = titulo; }

    public String getAutor() { return autor; }
    public void setAutor(String autor) { this.autor = autor; }

    public int getNumEjemplares() { return numEjemplares; }
    public void setNumEjemplares(int numEjemplares) { this.numEjemplares = numEjemplares; }

    public int getNumPrestados() { return numPrestados; }
    public void setNumPrestados(int numPrestados) { this.numPrestados = numPrestados; }

    public boolean prestar() {
        if (numPrestados < numEjemplares) {
            numPrestados++;
            return true;
        }
        return false;
    }

    public boolean devolver() {
        if (numPrestados > 0) {
            numPrestados--;
            return true;
        }
        return false;
    }

    @Override
    public String toString() {
        return "Título: " + titulo +
               ", Autor: " + autor +
               ", Ejemplares: " + numEjemplares +

               public class Main {
    public static void main(String[] args) {

        Libro libro1 = new Libro("Cien años de soledad", "Gabriel García Márquez", 5, 2);

        Libro libro2 = new Libro();
        libro2.setTitulo("El Principito");
        libro2.setAutor("Antoine de Saint-Exupéry");
        libro2.setNumEjemplares(3);
        libro2.setNumPrestados(1);

        System.out.println("=== Datos Iniciales ===");
        System.out.println(libro1);
        System.out.println(libro2);

        System.out.println("\n=== Pruebas libro1 ===");
        System.out.println("¿Se prestó?: " + libro1.prestar());
        System.out.println("¿Se devolvió?: " + libro1.devolver());
        System.out.println(libro1);

        System.out.println("\n=== Pruebas libro2 ===");
        System.out.println("¿Se prestó?: " + libro2.prestar());
        System.out.println("¿Se devolvió?: " + libro2.devolver());
        System.out.println(libro2);
    }
}
               ", Prestados: " + numPrestados;
    }
}
