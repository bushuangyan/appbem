# appbem
public class Test {

	public static void main(String[] args)  {
		// TODO Auto-generated method stub
		//通过字符流读取文件内容
		Reader r = null;
		Writer w = null;
		char[] cbuf = new char[5];
		try {
			r = new FileReader(new File("D://test.txt"));
			w = new FileWriter( new File("D://copy.txt"));
			int len = r.read(cbuf);
			w.write(cbuf);
			System.out.println(new String(cbuf, 0, len));
						
			r.close();
			w.close();
		} catch (FileNotFoundException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		} catch (IOException e) {
			// TODO Auto-generated catch block
			e.printStackTrace();
		}
	


	}

}
