# De8
% thiet ke mot he thong simulink de giai phuong trinh vi phan voi a la so
% cuoi cung cua ma sinh vien, neu so cuoi cung cua ma sinh vien bang khong
% thi dat a = 2
% aty''(t)+y(t)=e^-t

%bai 2 
% Viet ham tim nghiem phuong trinh vi phan theo phuong phap euler bien doi
% trong khoang tu a den b voi du doan ban dau Y(0)=0, co buoc h=abs(a-b)/25
% Ap dung cho phuong trinh y'(t) = ay(t)+e^(-by(t)) voi a b la hai so cuoi
% cua ma sinh vien. Neu so cuoi trung nhau thi b=a+3

a=1;
b=5;
h=abs(1-5)/25;
y0=0;
klast=8; % ta lay 8 gia tri
y=zeros(1,length(klast)); %tao mang 8 gia tri de luu bien
y(1)=y0;                  % Vì mảng bắt đầu từ 1 nên lưu giá trị y0 = y(1);
for k=2:klast+1           % sử dụng phương pháp euler-cauchy https://dangcnd.files.wordpress.com/2009/08/pptc6.pdf
    y1=y(k-1) +(h*(a*y(k-1)+exp(-b*y(k-1))));   % u= yi+h*f(xi,yi) vì ko có x nên ta bỏ chỉ còn u=yi+f(yi)
    diff=1;                                     % 
    while abs(diff)>0.005
        y2=y(k-1)+(h/2*(a*y(k-1)+exp(-b*y(k-1)))+(a*y(1)+exp(-b*y(1))));  %v = y(i-1)*h/2*(f(y(i-1))+f(u))
        diff = y1-y2;   y1 = y2;                                          % neu abs(v-u) < 0.005 thi gan u=v va tinh lại v;
     end
        y(k) = y1
end
