# KDV-Tutari-Hesaplayan-Program
Patika.dev > Java101 > Pratik2 - KDV Tutarı Hesaplayan Program

## Java ile kullanıcıdan alınan para değerinin KDV'li fiyatını ve KDV tutarını hesaplayıp ekrana bastıran programı yazın. 
* (Not : KDV tutarını 18% olarak alın)
* KDV'siz Fiyat = 10; 
* KDV'li Fiyat = 11.8; 
* KDV tutarı = 1.8;
* Eğer girilen tutar 0 ve 1000 TL arasında ise KDV oranı %18 , tutar 1000 TL'den büyük ise KDV oranını %8 olarak KDV tutarı hesaplayan programı yazınız.

import java.util.*;
public class pratik2;
	public static void main(String[] args) {
		//Kullanıcıdan para değerini al.
		System.out.println("Ücret miktarını giriniz: ");
		int miktar = sc.nextInt();
		
		// KDV hesaplamalarını tanımla.
		double kdv18 = (int)((miktar * 0.18) * 100) / 100.0;
		double kdv8 = (int)((miktar * 0.08) * 100) / 100.0;
		
		//Koşulları oluştur.
		if (miktar > 0 && miktar < 1000)
			System.out.println("KDV oranı %18\n"
					+ "KDV tutarı: "+ kdv18
					+ "\nKDV'siz fiyat: " + miktar
					+ "\nKDV'li fiyat: " + (miktar + kdv18));
	  
	  	else if (miktar > 1000)
			System.out.println("KDV oranı %8\n"
					+ "KDV tutarı: "+ kdv8
					+ "\nKDV'siz fiyat: " + miktar
			 		+ "\nKDV'li fiyat: " + (miktar + kdv8));
	}
}
