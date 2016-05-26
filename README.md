import java.util.*;
public class MyThread implements Runnable  {
private final long counter;

public MyThread(long counter) {
    this.counter = counter;
  }

  @Override
  public void run() {
    Random randomGenerator = new Random();
      int randomInt = randomGenerator.nextInt(10);
  System.out.println(randomInt);
  }
}


public class MainProcess {

	public static void main(String[] args) {
		for (int i = 0; i < 10; i++) {
		      Runnable T1 = new MyThread(50L + i);
		      Thread dice = new Thread(T1);
		      dice.setName(String.valueOf(100));
		      dice.start();
		}
	      }
}
