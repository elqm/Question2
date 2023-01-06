# Question2

5 ~ 15 사이 두 개의 난수를 발생시켜 두 난수 사이의 값의 총합을 구하라.
동일한 값일 경우 "다시 실행하세요."라는 문구를 출력하고 종료하라.
======= 출력 예시 =======
난수1 : 11
난수2 : 6
총합 : 51

	package com.greedy.section02.looping;

	public class Question {

	public static void main(String[] args) {

		/* 5 ~ 15 사이 두 개의 난수를 발생시켜 
		 * 두 난수 사이의 값의 총합을 구하라
		 * 동일한 값일 경우 "다시 실행하세요."라는 문구를 출력하고 종료하라.
		 * ======= 출력 예시 =======
		 * 난수1 : 11
		 * 난수2 : 6
		 * 총합 : 51
		 * */
		
		int random1 = (int) (Math.random() * 11 + 5);
		System.out.println("난수1 : " + random1);
		int random2 = (int) (Math.random() * 11 + 5);
		System.out.println("난수2 : " + random2);
		int max = 0;
		int min = 0;
		int sum = 0;
		
		if(random1 > random2) {
			max = random1;
			min = random2;
		} else if(random2 > random1) {
			max = random2;
			min = random1;
		} else {
			System.out.println("다시 실행하세요.");
			return;
		}
		
		for(int i = min; i <= max; i++) {
			sum += i;
		}
		System.out.println("총합 : " + sum);
		
		
	}

	}
