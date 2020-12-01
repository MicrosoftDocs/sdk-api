---
UID: NF:gdiplusheaders.Image.GetPropertyItem
title: Image::GetPropertyItem (gdiplusheaders.h)
description: The Image::GetPropertyItem method gets a specified property item (piece of metadata) from this Image object.
helpviewer_keywords: ["GetPropertyItem","GetPropertyItem method [GDI+]","GetPropertyItem method [GDI+]","Image class","Image class [GDI+]","GetPropertyItem method","Image.GetPropertyItem","Image::GetPropertyItem","_gdiplus_CLASS_Image_GetPropertyItem_propId_propSize_buffer_","gdiplus._gdiplus_CLASS_Image_GetPropertyItem_propId_propSize_buffer_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetPropertyItem_propId_propSize_buffer_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getpropertyitem.htm
ms.date: 12/05/2018
ms.keywords: GetPropertyItem, GetPropertyItem method [GDI+], GetPropertyItem method [GDI+],Image class, Image class [GDI+],GetPropertyItem method, Image.GetPropertyItem, Image::GetPropertyItem, _gdiplus_CLASS_Image_GetPropertyItem_propId_propSize_buffer_, gdiplus._gdiplus_CLASS_Image_GetPropertyItem_propId_propSize_buffer_
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
 - Image::GetPropertyItem
 - gdiplusheaders/Image::GetPropertyItem
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
 - Image.GetPropertyItem
---

# Image::GetPropertyItem


## -description

The <b>Image::GetPropertyItem</b> method gets a specified property item (piece of metadata) from this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.

## -parameters

### -param propId [in]

Type: <b>PROPID</b>

Integer that identifies the property item to be retrieved.

### -param propSize [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the property item to be retrieved. Call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitemsize">Image::GetPropertyItemSize</a> method to determine the size.

### -param buffer [out]

Type: <b><a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a>*</b>

Pointer to a <a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a> object that receives the property item.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The <b>Image::GetPropertyItem</b> method returns a <a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a> object. Before you call 
				<b>Image::GetPropertyItem</b>, you must allocate a buffer large enough to receive that object — the size varies according to data type and value of the property item. You can call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitemsize">Image::GetPropertyItemSize</a> method of an 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object to get the size, in bytes, of the required buffer.


#### Examples



The following example creates an 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a JPEG file. The code gets the make of the camera that captured the image by passing the PropertyTagEquipMake constant to the <b>Image::GetPropertyItem</b> method of the 
						<b>Image</b> object.


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

   UINT size = 0;
   PropertyItem* propertyItem = NULL;
   Image* image = new Image(L"FakePhoto.jpg");

   // Assume that the image has a property item of type PropertyItemEquipMake.
   // Get the size of that property item.
   size = image->GetPropertyItemSize(PropertyTagEquipMake);

   // Allocate a buffer to receive the property item.
   propertyItem = (PropertyItem*)malloc(size);

   // Get the property item.
   image->GetPropertyItem(PropertyTagEquipMake, size, propertyItem);

   // Display the members of the retrieved PropertyItem object.
   printf("The length of the property item is %u.\n", propertyItem->length);
   printf("The data type of the property item is %u.\n", propertyItem->type);

   if(propertyItem->type == PropertyTagTypeASCII)
      printf("The value of the property item is %s.\n", propertyItem->value);

   free(propertyItem);
   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```


The preceding code, along with a particular file, FakePhoto.jpg, produced the following output. Note that the data type is 2, the value of the PropertyTagTypeASCII constant that is defined in Gdiplusimaging.h.


```cpp
The length of the property item is 17.
The data type of the property item is 2.
The value of the property item is Northwind Traders.
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems">Image::GetAllPropertyItems</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertycount">Image::GetPropertyCount</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist">Image::GetPropertyIdList</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitemsize">Image::GetPropertyItemSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertysize">Image::GetPropertySize</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-removepropertyitem">Image::RemovePropertyItem</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem">Image::SetPropertyItem</a>



<a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a>



<a href="/windows/desktop/gdiplus/-gdiplus-reading-and-writing-metadata-use">Reading and Writing Metadata</a>