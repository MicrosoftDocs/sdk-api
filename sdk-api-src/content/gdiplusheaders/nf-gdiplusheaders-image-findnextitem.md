---
UID: NF:gdiplusheaders.Image.FindNextItem
title: Image::FindNextItem (gdiplusheaders.h)
description: The Image::FindNextItem method is used along with the Image::FindFirstItem method to enumerate the metadata items stored in this Image object.
helpviewer_keywords: ["FindNextItem","FindNextItem method [GDI+]","FindNextItem method [GDI+]","Image class","Image class [GDI+]","FindNextItem method","Image.FindNextItem","Image::FindNextItem","_gdiplus_CLASS_Image_FindNextItem_","gdiplus._gdiplus_CLASS_Image_FindNextItem_"]
old-location: gdiplus\_gdiplus_CLASS_Image_FindNextItem_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\findnextitem.htm
ms.date: 12/05/2018
ms.keywords: FindNextItem, FindNextItem method [GDI+], FindNextItem method [GDI+],Image class, Image class [GDI+],FindNextItem method, Image.FindNextItem, Image::FindNextItem, _gdiplus_CLASS_Image_FindNextItem_, gdiplus._gdiplus_CLASS_Image_FindNextItem_
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Image::FindNextItem
 - gdiplusheaders/Image::FindNextItem
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
 - Image.FindNextItem
---

# Image::FindNextItem


## -description

The <b>Image::FindNextItem</b> method is used along with the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-findfirstitem">Image::FindFirstItem</a> method to enumerate the metadata items stored in this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object. The <b>Image::FindNextItem</b> method retrieves the description and the data size of the next metadata item in this <b>Image</b> object.

## -parameters

### -param item [in, out]

Type: <b><a href="/previous-versions/ms534468(v=vs.85)">ImageItemData</a>*</b>

Pointer to an <a href="/previous-versions/ms534468(v=vs.85)">ImageItemData</a> object. On input, the Desc member points to a buffer (allocated by the caller) large enough to hold the metadata description (1 byte for JPEG, 4 bytes for PNG, 11 bytes for GIF), and the DescSize member specifies the size (1, 4, or 6) of the buffer pointed to by Desc. On output, the buffer pointed to by Desc receives the metadata description, and the DataSize member receives the size, in bytes, of the metadata itself.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-findfirstitem">Image::FindFirstItem</a> and <b>Image::FindNextItem</b> do not enumerate the metadata items stored by the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem">Image::SetPropertyItem</a> method.


#### Examples



The following example displays the description and data size for each metadata item in an Image object.


```cpp
Status stat;        
Image image(L"River5.png");

CHAR descBuf[5] = {0, 0, 0, 0, 0};
ImageItemData itemData;
ZeroMemory(&itemData, sizeof(itemData));
itemData.Size = sizeof(itemData);
itemData.DescSize = 4;
itemData.Desc = descBuf;

stat = image.FindFirstItem(&itemData);

while(Ok == stat)
{
   printf("%s   %d\n", itemData.Desc, itemData.DataSize);
   stat = image.FindNextItem(&itemData);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getitemdata">Image::GetItemData</a>