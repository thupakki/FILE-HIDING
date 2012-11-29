Hello everyone!!! this is ARJUN A from BANGALORE,INDIA


This is a C++ program to hide a file inside a bitmap file.

The bitmap here should be true color RGB image.other wise a file cannot be inserted into a bitmap. 


This program includes two header files:-
1)iostream.h
2)windows.h


windows.h header is used for handling files & bitmap reading.


This program contains two functions:-
i)to insert a file into bitmap i.e, insert_into_bitmap(char *bitmap,char *filename)
ii) to extract file from bitmap. i.e;extract_file_from_image(char *bitmapfile,char *actualfile)

I used here 9 global variables
1)file_header_bitmap:- this variable contains file size information of type BITMAPFILEHEADER in windows.h.
2)bih:- this variable contains height,width & color depth of the bitmap image.it is of type BITMAPINFOHEADER in windows.h.
3)data:-It is a pointer  to bitmap image data in memory.
4)source:-It is a ponter to source data in memory.
5)filehandler:-use to handle file on disk.It is of type HANDLE which is in windows.h.
6)read:-Byte read result.It is of type DWORD which is in windows.h.
7)written:-Byte written result.It is of type DWORD which is in windows.h.
8)data_size:-indicate size of data to be insert into bitmap.It is of type DWORD which is in windows.h.
9)file_size:-indicates the size of file .It is of type DWORD which is in windows.h.

Inbuilt functions used in this program:-

i)Createfile():- used to create a file or bitmap file.To know their parameters please go to this URL "http://msdn.microsoft.com/en-us/library/windows/desktop/aa363858(v=vs.85).aspx"
for more details

2)ReadFile():-used to read a file or bitmap file.To know their parameters please go to this URL "http://msdn.microsoft.com/en-us/library/windows/desktop/aa365467(v=vs.85).aspx"
 for more details
 
3)CloseHandle(filehandler):-used to close handler for the specified file handler.


Then,
bih.height:-indicates the height of the bitmap image.
bih.width:-indicates the width of the bitmap image.
bih.biXPelsPerMeter:-indicates the size of a file which is hidden in a bitmap.
bih.biBitCount:-used to check whether the image is 24 bit true color RGB image.
