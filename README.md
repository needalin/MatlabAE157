
 
     # MatlabAE157HW2
 
     %AE 157 Homework Assignment 2 Question #3

      clear all;

      clf;
      syms A B C D y t x

      %the code below is for Q#3 part c

      A = [-0.8 -1.5; 5.7 0]; % matix A

      B = [1.1 1.1; 1.1 0]; % matix B

      C = [4.9 1.5]; % matix C obtained from question #3 part a

      D = [2.2 1.1]; % matix D obtained from question #3 part b

      sys = ss(A,B,C,D)


      %the code below is for part d

      sys1 = tf(sys) %transfer function 1 
			sys2 = tf(sys1) %transfer function 2 
      sys3 = tf(sys2) %transfer function 3 
      sys4 = tf(sys3)	 %transfer function 4 
      %the code below is for part e

      [y, t] = step(A,B,C,D) %or you can use sys = step(A,B,C,D) - depends on system (dynamic vs steady state)


      %the code below is for part f

       [y, t] = impulse(A,B,C,D) 
       impulseplot(sys) %this makes a pretty graph of the impulse:)
     
