package doCwiczenia;

public class test {
    public static void main(String[] args) {
        int[] mat = new int[]{4, 5, 6, 6};
        int[] pl = new int[]{3, 2, 5, 4, 3, 5, 4};
        int[] ang = new int[]{3, 4, 5, 6};
        int[] fiz = new int[]{4, 5, 6, 5};
        drukuj("mat", srednia(mat));
        drukuj("pl", srednia(pl));
        drukuj("ang", srednia(ang));
        drukuj("fiz", srednia(fiz));
        double[] szkola = new double[]{srednia(mat), srednia(pl), srednia(ang), srednia(fiz)};
        drukujdo("wszystkich ocen cząstkowych", sredniado(szkola));
        int[] oceny=new int[]{ocKon(srednia(mat)), ocKon(srednia(pl)),ocKon(srednia(ang)), ocKon(srednia(fiz))};
        drukuj("ocen koncowych",srednia(oceny));


    }

    public static double srednia(int[] tab) {
        int suma = 0;
        for (int i : tab)
            suma += i;
        //for(int i=0; i<tab.length; i++)
        //    suma+=tab[i];
        //System.out.println(suma);
        //System.out.println(tab.length);
        return (double) suma / tab.length;
    }

    public static void drukuj(String nazw, double sr) {
        System.out.println("srednia z " + nazw + " to: " + sr);
    }

    public static double sredniado(double[] tab) {
        double suma = 0;
        for (double i : tab)
            suma += i;
        //for(int i=0; i<tab.length; i++)
        //    suma+=tab[i];
        //System.out.println(suma);
        //System.out.println(tab.length);
        return suma / tab.length;
    }

    public static void drukujdo(String nazw, double sr) {
        System.out.println("srednia z " + nazw + " to: " + sr);
    }

    public static int ocKon (double sr){
        if(sr<2.5)
            return 2;
        else if (sr<3.5)
            return 3;
        else if (sr<4.5)
            return 4;
        else return 5;
    }
}

