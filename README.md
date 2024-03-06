public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner scan = new Scanner(System.in);
        float toplamKilo = 0; 
        float toplamBoy = 0;
        
        for(int i = 1; i <= 5; i++) {
            System.out.println(i + ". Kişinin bilgileri:");
            System.out.print("Boyunuzu  giriniz: ");
            double boy = scan.nextDouble();
            System.out.print("Kilonuzu giriniz: ");
            float kilo = scan.nextFloat();
            toplamKilo += kilo; 
            
            double vki = kilo / (boy * boy);
            System.out.println("Vücut Kitle İndeksiniz = " + vki);
            
            String durum;
            if(vki < 18.5) {
                durum = "Zayıf";
            } else if(vki < 24.9) {
                durum = "Normal";
            } else if(vki < 29.9) {
                durum = "Hafif Şişman";
            } else if(vki < 39.9) {
                durum = "Şişman";
            } else {
                durum = "Obez";
            }
            System.out.println("Kişinin Beden Kütle İndeksi: " + vki + " Durumu: " + durum + "\n");
        }
        
        float ortalamaKilo = toplamKilo / 5; 
        float ortalamaBoy = toplamBoy / 5;
        System.out.println("Girilen 5 kişinin kilo ortalaması = " + ortalamaKilo);
        System.out.println("Girilen 5 kişinin Boy ortalaması = " + ortalamaBoy);      
	}

}
