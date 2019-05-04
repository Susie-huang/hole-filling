# hole-filling
matlab code about fill the hole of binary image，become the hole form 0 to 255 (pixels)
img = imread('000.jpg');

if ndims(img)==3

 img = rgb2gray(img);

end

img_bw = im2bw(img);

img_fill = imfill(img_bw, 'holes');

figure;

subplot(1,2,1),imshow(img_bw), title('有空洞的图像');

subplot(1,2,2),imshow(img_fill), title('孔洞被填充的图像');
