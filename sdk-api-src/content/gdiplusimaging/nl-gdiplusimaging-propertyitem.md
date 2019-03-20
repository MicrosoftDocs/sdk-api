---
UID: NL:gdiplusimaging.PropertyItem
title: PropertyItem (gdiplusimaging.h)
author: windows-sdk-content
description: The PropertyItem class is a helper class for the Image and Bitmap classes. A PropertyItem object holds one piece of image metadata.
old-location: gdiplus\_gdiplus_CLASS_PropertyItem_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\propertyitem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropertyItem, PropertyItem class [GDI+], PropertyItem class [GDI+],described, _gdiplus_CLASS_PropertyItem_Class, gdiplus._gdiplus_CLASS_PropertyItem_Class, gdiplusimaging/PropertyItem
ms.topic: class
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PropertyItem class


## -description


The <b>PropertyItem</b> class is a helper class for the 
			<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> and 
			<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> classes. A <b>PropertyItem</b> object holds one piece of image metadata.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">PropertyItem</b> has these types of members:


## -remarks



To set a property item (piece of metadata), pass the address of a <b>PropertyItem</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms535405(v=VS.85).aspx">Image::SetPropertyItem</a> method of an 
				<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object. To retrieve a property item, pass the address of a <b>PropertyItem</b> object to the <a href="https://msdn.microsoft.com/en-us/library/ms535390(v=VS.85).aspx">Image::GetPropertyItem</a> method of an 
				<b>Image</b> object.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535372(v=VS.85).aspx">Image::GetAllPropertyItems</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535389(v=VS.85).aspx">Image::GetPropertyIdList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535390(v=VS.85).aspx">Image::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535391(v=VS.85).aspx">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535392(v=VS.85).aspx">Image::GetPropertySize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535400(v=VS.85).aspx">Image::RemovePropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535405(v=VS.85).aspx">Image::SetPropertyItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533832(v=VS.85).aspx">Reading and Writing Metadata</a>
 

 

