---
UID: NF:gdiplusheaders.Image.GetAllPropertyItems
title: Image::GetAllPropertyItems (gdiplusheaders.h)
description: The Image::GetAllPropertyItems method gets all the property items (metadata) stored in this Image object.
helpviewer_keywords: ["GetAllPropertyItems","GetAllPropertyItems method [GDI+]","GetAllPropertyItems method [GDI+]","Image class","Image class [GDI+]","GetAllPropertyItems method","Image.GetAllPropertyItems","Image::GetAllPropertyItems","_gdiplus_CLASS_Image_GetAllPropertyItems_totalBufferSize_numProperties_allItems_","gdiplus._gdiplus_CLASS_Image_GetAllPropertyItems_totalBufferSize_numProperties_allItems_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetAllPropertyItems_totalBufferSize_numProperties_allItems_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getallpropertyitems.htm
ms.date: 12/05/2018
ms.keywords: GetAllPropertyItems, GetAllPropertyItems method [GDI+], GetAllPropertyItems method [GDI+],Image class, Image class [GDI+],GetAllPropertyItems method, Image.GetAllPropertyItems, Image::GetAllPropertyItems, _gdiplus_CLASS_Image_GetAllPropertyItems_totalBufferSize_numProperties_allItems_, gdiplus._gdiplus_CLASS_Image_GetAllPropertyItems_totalBufferSize_numProperties_allItems_
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
 - Image::GetAllPropertyItems
 - gdiplusheaders/Image::GetAllPropertyItems
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
 - Image.GetAllPropertyItems
---

# Image::GetAllPropertyItems


## -description

The <b>Image::GetAllPropertyItems</b> method gets all the property items (metadata) stored in this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.

## -parameters

### -param totalBufferSize [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the 
					<i>allItems</i> buffer. Call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertysize">Image::GetPropertySize</a> method to obtain the required size.

### -param numProperties [in]

Type: <b>UINT</b>

Integer that specifies the number of properties in the image. Call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertysize">Image::GetPropertySize</a> method to obtain this number.

### -param allItems [out]

Type: <b><a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a>*</b>

Pointer to an array of <a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a> objects that receives the property items.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Status</b> enumeration.

## -remarks

Some image files contain metadata that you can read to determine features of the image. For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.

GDI+ stores an individual piece of metadata in a <a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a> object. The <b>Image::GetAllPropertyItems</b> method returns an array of <b>PropertyItem</b> objects. Before you call <b>Image::GetAllPropertyItems</b>, you must allocate a buffer large enough to receive that array. You can call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertysize">Image::GetPropertySize</a> method of an 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object to get the size, in bytes, of the required buffer. The <b>Image::GetPropertySize</b> method also gives you the number of properties (pieces of metadata) in the image.

Several enumerations and constants related to image metadata are defined in Gdiplusimaging.h.


#### Examples



The following example creates an 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a JPEG file. The code calls the <b>GetAllPropertyItems</b> method of that 
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

// Print the id data member of each property item.
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


The preceding output shows a hexadecimal ID number for each property item. You can look up those ID numbers in Gdiplusimaging.h and find out that they represent the following property tags.

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



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertycount">Image::GetPropertyCount</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist">Image::GetPropertyIdList</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem">Image::GetPropertyItem</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitemsize">Image::GetPropertyItemSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertysize">Image::GetPropertySize</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-removepropertyitem">Image::RemovePropertyItem</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem">Image::SetPropertyItem</a>



<a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a>



<a href="/windows/desktop/gdiplus/-gdiplus-reading-and-writing-metadata-use">Reading and Writing Metadata</a>