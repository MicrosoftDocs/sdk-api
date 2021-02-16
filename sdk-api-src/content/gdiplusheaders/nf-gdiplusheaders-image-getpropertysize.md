---
UID: NF:gdiplusheaders.Image.GetPropertySize
title: Image::GetPropertySize (gdiplusheaders.h)
description: The Image::GetPropertySize method gets the total size, in bytes, of all the property items stored in this Image object. The Image::GetPropertySize method also gets the number of property items stored in this Image object.
helpviewer_keywords: ["GetPropertySize","GetPropertySize method [GDI+]","GetPropertySize method [GDI+]","Image class","Image class [GDI+]","GetPropertySize method","Image.GetPropertySize","Image::GetPropertySize","_gdiplus_CLASS_Image_GetPropertySize_totalBufferSize_numProperties_","gdiplus._gdiplus_CLASS_Image_GetPropertySize_totalBufferSize_numProperties_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetPropertySize_totalBufferSize_numProperties_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getpropertysize.htm
ms.date: 12/05/2018
ms.keywords: GetPropertySize, GetPropertySize method [GDI+], GetPropertySize method [GDI+],Image class, Image class [GDI+],GetPropertySize method, Image.GetPropertySize, Image::GetPropertySize, _gdiplus_CLASS_Image_GetPropertySize_totalBufferSize_numProperties_, gdiplus._gdiplus_CLASS_Image_GetPropertySize_totalBufferSize_numProperties_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Image::GetPropertySize
 - gdiplusheaders/Image::GetPropertySize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.GetPropertySize
---

# Image::GetPropertySize


## -description

The <b>Image::GetPropertySize</b> method gets the total size, in bytes, of all the property items stored in this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object. The <b>Image::GetPropertySize</b> method also gets the number of property items stored in this 
			<b>Image</b> object.

## -parameters

### -param totalBufferSize [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the total size, in bytes, of all the property items.

### -param numProperties [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the number of property items.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Windows GDI+ stores an individual piece of metadata in a <a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a> object. The <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems">Image::GetAllPropertyItems</a> method returns an array of <b>PropertyItem</b> objects. Before you call <b>Image::GetAllPropertyItems</b>, you must allocate a buffer large enough to receive that array. You can call the <b>Image::GetPropertySize</b> method of an 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object to get the size, in bytes, of the required buffer. The <b>Image::GetPropertySize</b> method also gives you the number of properties (pieces of metadata) in the image.


#### Examples



The following example creates an 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a JPEG file. The code calls the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems">Image::GetAllPropertyItems</a> method of that 
						<b>Image</b> object to obtain its property items (metadata).


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

   // Create an Image object based on a JPEG file.
   Image* image = new Image(L"FakePhoto.jpg"); 

  // Find out how many property items are in the image, and find out the
   // required size of the buffer that will receive those property items.
   UINT totalBufferSize;
   UINT numProperties;
   image->GetPropertySize(&totalBufferSize, &numProperties);

   // Allocate the buffer that will receive the property items.
   PropertyItem* pAllItems = (PropertyItem*)malloc(totalBufferSize);

   // Fill the buffer.
   image->GetAllPropertyItems(totalBufferSize, numProperties, pAllItems);

   // Print the ID of each property item.
   for(UINT j = 0; j < numProperties; ++j)
   {
      printf("%x\n", pAllItems[j].id);
   }

   free(pAllItems);
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

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems">Image::GetAllPropertyItems</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertycount">Image::GetPropertyCount</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist">Image::GetPropertyIdList</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem">Image::GetPropertyItem</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitemsize">Image::GetPropertyItemSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-removepropertyitem">Image::RemovePropertyItem</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem">Image::SetPropertyItem</a>



<a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a>



<a href="/windows/desktop/gdiplus/-gdiplus-reading-and-writing-metadata-use">Reading and Writing Metadata</a>