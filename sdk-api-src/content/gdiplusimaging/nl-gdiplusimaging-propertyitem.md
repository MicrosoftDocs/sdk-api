---
UID: NL:gdiplusimaging.PropertyItem
title: PropertyItem (gdiplusimaging.h)
description: The PropertyItem class is a helper class for the Image and Bitmap classes. A PropertyItem object holds one piece of image metadata.
old-location: gdiplus\_gdiplus_CLASS_PropertyItem_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\propertyitem.htm
ms.date: 12/05/2018
ms.keywords: PropertyItem, PropertyItem class [GDI+], PropertyItem class [GDI+],described, _gdiplus_CLASS_PropertyItem_Class, gdiplus._gdiplus_CLASS_PropertyItem_Class, gdiplusimaging/PropertyItem
f1_keywords:
- gdiplusimaging/PropertyItem
dev_langs:
- c++
req.header: gdiplusimaging.h
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.lib
- Gdiplus.dll
api_name:
- PropertyItem
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# PropertyItem class


## -description


The <b>PropertyItem</b> class is a helper class for the 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> and 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> classes. A <b>PropertyItem</b> object holds one piece of image metadata.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">PropertyItem</b> has these types of members:


## -remarks



To set a property item (piece of metadata), pass the address of a <b>PropertyItem</b> object to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem">Image::SetPropertyItem</a> method of an 
				<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object. To retrieve a property item, pass the address of a <b>PropertyItem</b> object to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem">Image::GetPropertyItem</a> method of an 
				<b>Image</b> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems">Image::GetAllPropertyItems</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist">Image::GetPropertyIdList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem">Image::GetPropertyItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertyitemsize">Image::GetPropertyItemSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getpropertysize">Image::GetPropertySize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-removepropertyitem">Image::RemovePropertyItem</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem">Image::SetPropertyItem</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-reading-and-writing-metadata-use">Reading and Writing Metadata</a>
 

 

