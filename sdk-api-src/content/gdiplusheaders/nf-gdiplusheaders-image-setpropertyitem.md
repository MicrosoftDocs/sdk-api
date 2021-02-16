---
UID: NF:gdiplusheaders.Image.SetPropertyItem
title: Image::SetPropertyItem (gdiplusheaders.h)
description: The Image::SetPropertyItem method sets a property item (piece of metadata) for this Image object. If the item already exists, then its contents are updated; otherwise, a new item is added.
helpviewer_keywords: ["Image class [GDI+]","SetPropertyItem method","Image.SetPropertyItem","Image::SetPropertyItem","SetPropertyItem","SetPropertyItem method [GDI+]","SetPropertyItem method [GDI+]","Image class","_gdiplus_CLASS_Image_SetPropertyItem_item_","gdiplus._gdiplus_CLASS_Image_SetPropertyItem_item_"]
old-location: gdiplus\_gdiplus_CLASS_Image_SetPropertyItem_item_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\setpropertyitem.htm
ms.date: 12/05/2018
ms.keywords: Image class [GDI+],SetPropertyItem method, Image.SetPropertyItem, Image::SetPropertyItem, SetPropertyItem, SetPropertyItem method [GDI+], SetPropertyItem method [GDI+],Image class, _gdiplus_CLASS_Image_SetPropertyItem_item_, gdiplus._gdiplus_CLASS_Image_SetPropertyItem_item_
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
 - Image::SetPropertyItem
 - gdiplusheaders/Image::SetPropertyItem
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
 - Image.SetPropertyItem
---

# Image::SetPropertyItem


## -description

The <b>Image::SetPropertyItem</b> method sets a property item (piece of metadata) for this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object. If the item already exists, then its contents are updated; otherwise, a new item is added.

## -parameters

### -param item [in]

Type: <b>const PropertyItem*</b>

Pointer to a <a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a> object that specifies the property item to be set.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Certain image formats (for example, ICON and EMF) don't support properties. If you call the <b>Image::SetPropertyItem</b> method on an image that doesn't support properties, it will return PropertyNotSupported.


#### Examples



The following console application creates a 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a JPEG file. The code calls the <b>Image::SetPropertyItem</b> method of that 
						<b>Image</b> object to set the title of the image. Then the code retrieves and displays the new title.


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

   // Set the image title.
   PropertyItem* propItem = new PropertyItem;
   CHAR newTitleValue[] = "Fake Photograph 2";

   propItem->id = PropertyTagImageTitle;
   propItem->length = 18;  //  includes null terminator
   propItem->type = PropertyTagTypeASCII;
   propItem->value = newTitleValue;

   image->SetPropertyItem(propItem);

   // Get and display the new image title.
   UINT size = image->GetPropertyItemSize(PropertyTagImageTitle);
   PropertyItem* title = (PropertyItem*)malloc(size);
   image->GetPropertyItem(PropertyTagImageTitle, size, title);
   printf("The image title is %s.\n", title->value);

   free(title);
   delete propItem;
   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertycount">Image::GetPropertyCount</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist">Image::GetPropertyIdList</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem">Image::GetPropertyItem</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitemsize">Image::GetPropertyItemSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertysize">Image::GetPropertySize</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-removepropertyitem">Image::RemovePropertyItem</a>



<a href="/previous-versions/ms534493(v=vs.85)">PropertyItem</a>



<a href="/windows/desktop/gdiplus/-gdiplus-reading-and-writing-metadata-use">Reading and Writing Metadata</a>