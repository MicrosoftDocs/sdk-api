---
UID: NF:gdiplusheaders.Image.SetPropertyItem
title: Image::SetPropertyItem
author: windows-sdk-content
description: The Image::SetPropertyItem method sets a property item (piece of metadata) for this Image object. If the item already exists, then its contents are updated; otherwise, a new item is added.
old-location: gdiplus\_gdiplus_CLASS_Image_SetPropertyItem_item_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\setpropertyitem.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Image class [GDI+],SetPropertyItem method, Image.SetPropertyItem, Image::SetPropertyItem, SetPropertyItem, SetPropertyItem method [GDI+], SetPropertyItem method [GDI+],Image class, _gdiplus_CLASS_Image_SetPropertyItem_item_, gdiplus._gdiplus_CLASS_Image_SetPropertyItem_item_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.SetPropertyItem
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Image::SetPropertyItem


## -description


The <b>Image::SetPropertyItem</b> method sets a property item (piece of metadata) for this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object. If the item already exists, then its contents are updated; otherwise, a new item is added.


## -parameters




### -param item [in]

Type: <b>const PropertyItem*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534493(v=VS.85).aspx">PropertyItem</a> object that specifies the property item to be set. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



Certain image formats (for example, ICON and EMF) don't support properties. If you call the <b>Image::SetPropertyItem</b> method on an image that doesn't support properties, it will return PropertyNotSupported.


#### Examples



The following console application creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object based on a JPEG file. The code calls the <b>Image::SetPropertyItem</b> method of that 
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




<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535388(v=VS.85).aspx">Image::GetPropertyCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535389(v=VS.85).aspx">Image::GetPropertyIdList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535390(v=VS.85).aspx">Image::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535391(v=VS.85).aspx">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535392(v=VS.85).aspx">Image::GetPropertySize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535400(v=VS.85).aspx">Image::RemovePropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534493(v=VS.85).aspx">PropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533832(v=VS.85).aspx">Reading and Writing Metadata</a>
 

 

