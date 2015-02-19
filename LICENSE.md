import java.io.ObjectInputStream.GetField;
import java.util.Scanner;

public class Fatura<quantComprada> {
	private String numero;
	private String descricao;
	private static int quantComprada;
	private static double precoItem;

	public static void getValorFatura() {

		double valor = quantComprada * precoItem;
		if (valor >= 0.0) {
			valor = 0.0;

		}else{
			System.out.println("Valor: " + valor);
		}
		

		return;

	}

	public static void main(String[] args) {

		Scanner scan = new Scanner(System.in);

		quantComprada = scan.nextInt();
		precoItem = scan.nextDouble();

		System.out.println("Quantidade comprada:" + quantComprada);
		System.out.println("Preço do Item: " + precoItem);
		getValorFatura();
		return;

	}
}
