---
UID: NF:gdiplusheaders.Image.GetPropertyIdList
title: Image::GetPropertyIdList
author: windows-sdk-content
description: The Image::GetPropertyIdList method gets a list of the property identifiers used in the metadata of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetPropertyIdList_numOfProperty_list_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getpropertyidlist.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetPropertyIdList, GetPropertyIdList method [GDI+], GetPropertyIdList method [GDI+],Image class, Image class [GDI+],GetPropertyIdList method, Image.GetPropertyIdList, Image::GetPropertyIdList, _gdiplus_CLASS_Image_GetPropertyIdList_numOfProperty_list_, gdiplus._gdiplus_CLASS_Image_GetPropertyIdList_numOfProperty_list_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.GetPropertyIdList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Image.GetPropertyIdList
: 
req.product: GDI+ 1.0
---

# Image::GetPropertyIdList


## -description


The <b>Image::GetPropertyIdList</b> method gets a list of the property identifiers used in the metadata of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object.


## -parameters




### -param numOfProperty [in]

Type: <b>UINT</b>

Integer that specifies the number of elements in the 
					<i>list</i> array. Call the <a href="https://msdn.microsoft.com/en-us/library/ms535388(v=VS.85).aspx">Image::GetPropertyCount</a> method to determine this number. 


### -param list [out]

Type: <b>PROPID*</b>

Pointer to an array that receives the property identifiers. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



The <b>Image::GetPropertyIdList</b> method returns an array of 
				<b>PROPID</b>s. Before you call <b>Image::GetPropertyIdList</b>, you must allocate a buffer large enough to receive that array. You can call the <a href="https://msdn.microsoft.com/en-us/library/ms535388(v=VS.85).aspx">Image::GetPropertyCount</a> method of an 
				<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object to determine the size of the required buffer. The size of the buffer should be the return value of <b>Image::GetPropertyCount</b> multiplied by 
				<b>sizeof</b>(
				<b>PROPID</b>).


#### Examples



The following example creates an 
						<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object based on a JPEG file. The code calls the <b>Image::GetPropertyIdList</b> method of that 
						<b>Image</b> object to find out what types of metadata are stored in the image.


```cpp
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT count = 0; 
   Image* image = new Image(L"FakePhoto.jpg");

   // How many types of metadata are in the image?
   count = image->GetPropertyCount();
   if(count == 0)
      return 0;

   // Allocate a buffer to receive an array of PROPIDs.
   PROPID* propIDs = new PROPID[count];

   image->GetPropertyIdList(count, propIDs);

   // List the retrieved IDs.
   for(UINT j = 0; j < count; ++j)
      printf("%x\n", propIDs[j]);

   delete [] propIDs;
   delete image;   
  
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```


The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:


```cpp
320
10f
110
9003
829a
5090
5091
```


The preceding output shows the hexadecimal value of each property identifier. You can look up those numbers in Gdiplusimaging.h and find out that they represent the following property tags.


<table class="clsStd">
<tr>
<th>Hexadecimal value</th>
<th>Property tag</th>
</tr>
<tr>
<td>0x0320</td>
<td>PropertyTagImageTitle</td>
</tr>
<tr>
<td>0x010f</td>
<td>PropertyTagEquipMake</td>
</tr>
<tr>
<td>0x0110</td>
<td>PropertyTagEquipModel</td>
</tr>
<tr>
<td>0x9003</td>
<td>PropertyTagExifDTOriginal</td>
</tr>
<tr>
<td>0x829a</td>
<td>PropertyTagExifExposureTime</td>
</tr>
<tr>
<td>0x5090</td>
<td>PropertyTagLuminanceTable</td>
</tr>
<tr>
<td>0x5091</td>
<td>PropertyTagChrominanceTable</td>
</tr>
</table>
 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535372(v=VS.85).aspx">Image::GetAllPropertyItems</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535388(v=VS.85).aspx">Image::GetPropertyCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535390(v=VS.85).aspx">Image::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535391(v=VS.85).aspx">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535392(v=VS.85).aspx">Image::GetPropertySize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535400(v=VS.85).aspx">Image::RemovePropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535405(v=VS.85).aspx">Image::SetPropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534493(v=VS.85).aspx">PropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533832(v=VS.85).aspx">Reading and Writing Metadata</a>
 

 

