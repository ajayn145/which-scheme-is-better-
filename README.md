                                                                                 PRE-REQUISITES----->
taylor series------>

![image](https://user-images.githubusercontent.com/77200332/134895486-c20358a0-8d06-4b12-9abf-48d731181f51.png)
first derivative approximated FDM------->

![image](https://user-images.githubusercontent.com/77200332/134895647-7914400a-4b52-4dd8-aef5-050151b0ebaf.png)
first derivative approximated BDM------->

![image](https://user-images.githubusercontent.com/77200332/134895797-5d23a4ab-971c-464c-afd3-75e964aab0ff.png)
first derivative approximated CDM------->

![image](https://user-images.githubusercontent.com/77200332/134895952-099db558-9829-4496-bc53-8d022564ba07.png)
order of error--------->

![image](https://user-images.githubusercontent.com/77200332/134896171-9f6a7f1d-d98d-4836-b11c-b00dd3f4599b.png)


                                                                                 MAIN PROGRAM----------->      
# which-scheme-is-better-
This will tell us which scheme is better? - whether FDM (forward differencing Method), BDM (backward Differencing Method), or CDM (central differencing scheme).)

%%
%Finding First derivatives of a polynomial using FINITE DIFFERENCE METHOD

    close all
    clear all
    clc

%%
%defining the polynomial
    polynomial=[3 5 7]

%%
%finding derivative of a polynomial
    polynomial_derivative=polyder(polynomial)

%%
%finding value of a polynmial and its deriative at x = 0
    polynomial_value_with_x_as_0 = polyval(polynomial,0)
    polynomial_derivative_value_with_x_as_0 = polyval(polynomial_derivative,0)

%%
    x_0=0;
    h=linspace(0,1,50);

%%
    for i=1:length(h)


        %Finite Difference Method- Forward Difference Method (FDM)
        polynomial_first_derivative_using_FDM(i) =  polyval(polynomial,(x_0+h(i)))/(h(i))- polyval(polynomial,x_0)/(h(i));


        %Finite Difference Method- Backward Difference Method (BDM)
        polynomial_first_derivative_using_BDM(i) = polyval(polynomial,x_0)/(h(i)) - polyval(polynomial,(x_0-h(i)))/(h(i));


        %Finite Differece Method - Central Difference Method (CDM)
        polynomial_first_derivative_using_CDM(i) = polyval(polynomial,(x_0+h(i)))/(2*h(i)) - polyval(polynomial,(x_0-h(i)))/(2*h(i));

        figure(1)
        plot(polynomial_first_derivative_using_FDM,'k-o')
        hold on
        plot(polynomial_first_derivative_using_BDM,'k-d')
        plot(polynomial_first_derivative_using_CDM,'k-*')
        axis([1 51 0 10])
        text = 'Dependency of FDM, BDM,CDM on varying grid size- The graph shows the CDM is';
        text = [text newline 'better than FDM or BDM, as the error formation is less in CDM OR THIS POLYNOMIAL'];
        title(text)
        xlabel("gride space / mesh size / cell size")
        ylabel("first derivative of a ploynomial")
        legend("first derivative using FDM","first derivative using BDM","first derivative using CDM")
    end

%%
    display(polynomial_first_derivative_using_FDM)
    display(polynomial_first_derivative_using_BDM)
    display(polynomial_first_derivative_using_CDM)


%%
%Code in MATLAB
![image](https://user-images.githubusercontent.com/77200332/134783194-9782db23-e1aa-47da-9289-2225ec1377e9.png)
![image](https://user-images.githubusercontent.com/77200332/134783204-5fb80a4b-e6ab-459c-8c55-8e7f15a27f98.png)
![image](https://user-images.githubusercontent.com/77200332/134783211-f21950eb-ac10-43e3-b488-dacb9bffc40b.png)




%%
% output Files
![image](https://user-images.githubusercontent.com/77200332/134773958-b00c3bd9-9b4b-40d9-aed3-db4f5b1dadb4.png)
![image](https://user-images.githubusercontent.com/77200332/134773994-7c658509-9edf-42bc-99c7-1c591e8721ec.png)
![image](https://user-images.githubusercontent.com/77200332/134774020-84eef441-19c9-4174-9eb2-995e1717c9b3.png)

