---
draft: false
date: 2023-10-26
description: Định lý Chicken McNugget
categories:
  - Tôi yêu toán học
authors:
  - phieu07
slug: chicken-mcnugget-theorem
comments: true
---

# Định lý Chicken McNugget

Định lý Chicken McNugget (hoặc Bài toán tem bưu chính hoặc Bài toán đồng xu Frobenius) 
phát biểu rằng với hai số nguyên dương nguyên tố bất kỳ $m,n$, 
số nguyên lớn nhất không thể viết dưới dạng $am + bn$ cho các số nguyên không âm $a, b$ là $mn-m-n$.

<!-- more -->

Một hệ quả của định lý là có chính xác $\frac{(m - 1)(n - 1)}{2}$ số nguyên dương
không thể biểu diễn dưới dạng $am + bn$. 
Bằng chứng dựa trên thực tế là trong mỗi cặp có dạng $(k, mn-m-n-k)$, 
có chính xác một phần tử có thể biểu diễn được.

## Nguồn gốc
Có rất nhiều câu chuyện xung quanh nguồn gốc của định lý Chicken McNugget. 
Tuy nhiên, phổ biến nhất cho đến nay vẫn là Chicken McNugget. 

!!! info "Lorem ipsum"
    Ban đầu, McDonald's bán hàng theo gói **9** và **20**. Những người đam mê toán học tò mò tìm ra 
    số lượng gói hàng lớn nhất không thể mua được bằng các gói này, 
    từ đó tạo ra Định lý McNugget Gà (câu trả lời là 151 gói hàng). 
    ==Định lý Chicken McNugget== còn được gọi là ==Bài toán đồng xu Frobenius== hay ==Bài toán Frobenius==, 
    sau khi nhà toán học người Đức **Ferdinand Frobenius** hỏi về 
    số lượng tiền tệ lớn nhất không thể được tạo ra bằng một số loại tiền xu.

Bằng chứng không lời
$$
\begin{array}{ccccccc} 0\mod{m}&1\mod{m}&2\mod{m}&...&...&...&(m-1)\mod{m} \\ \hline \cancel{0n}&1&2&&...&&m-1\\ \cancel{0n+m}&...&&\vdots&&...&\\ \cancel{0n+2m}&...&& \cancel{1n}&&...&\\ \cancel{0n+3m}&&&\cancel{1n+m}&&\vdots&\\ \cancel{0n+4m}&&&\cancel{1n+2m}&&\cancel {2n}&\\ \cancel{0n+5m}&&&\cancel{1n+3m}&&\cancel{2n+m}&\\ \vdots&&&\vdots&&\vdots&\\ \cancel{\qquad}&\cancel{ \qquad}&\cancel{ \qquad}&\cancel{ \qquad}&\mathbf{(m-1)n-m}&\cancel{\qquad }&\cancel{\qquad }\\ \cancel{\qquad} &\cancel{\qquad}&\cancel{ \qquad}&\cancel{ \qquad}&\cancel{(m-1)n}&\cancel{\qquad }&\cancel{\qquad } \end{array }$$

## Bằng chứng 1
Sự định nghĩa. Một số nguyên $N \in \mathbb{Z}$ sẽ được gọi là có thể mua được nếu tồn tại các số nguyên không âm $a,b$ sao cho $am+bn = N$.

Chúng ta muốn chứng minh rằng $mn-m-n$ là số nguyên lớn nhất không thể mua được. Chúng tôi được yêu cầu phải chứng minh rằng:

(1) $mn-m-n$ không thể mua được

(2) Mọi $N > mn-m-n$ đều có thể mua được

Lưu ý rằng tất cả các số nguyên có thể mua được đều không âm, do đó tập hợp các số nguyên không thể mua được là khác rỗng.

Bổ đề. Giả sử $A_{N} \subset \mathbb{Z} \times \mathbb{Z}$ là tập hợp các nghiệm $(x,y)$ cho $xm+yn = N$. Khi đó $A_{N} = \{(x+kn,y-km) \;:\; k \in \mathbb{Z}\}$ với mọi $(x,y) \in A_{N}$.

Chứng minh: Theo bổ đề Bezout, tồn tại các số nguyên $x',y'$ sao cho $x'm+y'n = 1$. Khi đó $(Nx')m+(Ny')n = N$. Do đó $A_{N}$ không trống. Dễ dàng kiểm tra được $(Nx'+kn,Ny'-km) \in A_{N}$ với mọi $k \in \mathbb{Z}$. Bây giờ chúng ta chứng minh rằng không có ai khác. Giả sử $(x_{1},y_{1})$ và $(x_{2},y_{2})$ là nghiệm của $xm+yn=N$. Khi đó $x_{1}m+y_{1}n = x_{2}m+y_{2}n$ ngụ ý $m(x_{1}-x_{2}) = n(y_{2}-y_{ 1})$. Vì $m$ và $n$ là nguyên tố cùng nhau và $m$ chia $n(y_{2}-y_{1})$, $m$ chia $y_{2}-y_{1}$ và $y_{2 } \equiv y_{1} \pmod{m}$. Tương tự $x_{2} \equiv x_{1} \pmod{n}$. Đặt $k_{1},k_{2}$ là các số nguyên sao cho $x_{2}-x_{1} = k_{1}n$ và $y_{2}-y_{1} = k_{2}m $. Khi đó $m(-k_{1}n) = n(k_{2}m)$ ngụ ý $k_{1} = -k_{2}.$ Chúng ta có kết quả mong muốn. $\vuông$

Bổ đề. Với mọi số nguyên $N$, tồn tại duy nhất $(a_{N},b_{N}) \in \mathbb{Z} \times \{0,1,\ldots,m-1\}$ sao cho $a_ {N}m + b_{N}n = N$.

Chứng minh: Theo thuật toán chia, tồn tại một và chỉ một $k$ sao cho $0 \le y-km \le m-1$. $\vuông$

Bổ đề. $N$ có thể mua được khi và chỉ khi $a_{N} \ge 0$.

Chứng minh: Nếu $a_{N} \ge 0$, thì chúng ta có thể chỉ cần chọn $(a,b) = (a_{N},b_{N})$ để $N$ có thể mua được. Nếu $a_{N} < 0$, thì $a_{N}+kn < 0$ if $k \le 0$ và $b_{N}-km < 0$ nếu $k > 0$, do đó có ít nhất một tọa độ của $(a_{N}+kn,b_{N}-km)$ là âm đối với tất cả $k \in \mathbb{Z}$. Do đó $N$ không thể mua được. $\vuông$

Do đó, tập hợp các số nguyên không thể mua được là $\{xm+yn \;:\; x<0,0 \le y \le m-1\}$. Chúng tôi muốn tìm mức tối đa của tập hợp này. Vì cả $m,n$ đều dương, nên giá trị lớn nhất đạt được khi $x = -1$ và $y = m-1$ sao cho $xm+yn = (-1)m+(m-1)n = mn- m-n$.

Chứng minh 2
Chúng ta bắt đầu với phát biểu này được lấy từ Chứng minh 2 của Định lý nhỏ Fermat:

"Cho $S = \{1,2,3,\cdots, p-1\}$. Khi đó, ta khẳng định rằng tập $a \cdot S$, gồm tích các phần tử của $S$ với $ a$, lấy modulo $p$, đơn giản là một hoán vị của $S$. Nói cách khác,

\[S \equiv \{1a, 2a, \cdots, (p-1)a\} \pmod{p}.\]

Rõ ràng không có $ia$ nào của $1 \le i \le p-1$ chia hết cho $p$, vì vậy nó đủ để chỉ ra rằng tất cả các phần tử trong $a \cdot S$ là khác nhau. Giả sử $ai \equiv aj \pmod{p}$ cho $i \neq j$. Vì $\text{gcd}\, (a,p) = 1$, theo quy tắc hủy, điều đó rút gọn thành $i \equiv j \pmod{p}$, điều này mâu thuẫn."

Bởi vì $m$ và $n$ là nguyên tố cùng nhau, nên chúng ta biết rằng việc nhân các số dư của $m$ với $n$ chỉ đơn giản là hoán vị
