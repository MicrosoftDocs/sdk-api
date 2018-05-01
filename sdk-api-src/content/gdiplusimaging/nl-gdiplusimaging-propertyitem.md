---
UID: NL:gdiplusimaging.PropertyItem
title: PropertyItem
author: windows-driver-content
description: The PropertyItem class is a helper class for the Image and Bitmap classes. A PropertyItem object holds one piece of image metadata.
old-location: gdiplus\_gdiplus_CLASS_PropertyItem_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\propertyitem.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: PropertyItem, PropertyItem class [GDI+], PropertyItem class [GDI+], described, _gdiplus_CLASS_PropertyItem_Class, gdiplus._gdiplus_CLASS_PropertyItem_Class, gdiplusimaging/PropertyItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.lib
-	Gdiplus.dll
api_name:
-	PropertyItem
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# PropertyItem class


## -description


The <b>PropertyItem</b> class is a helper class for the 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> and 
			<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a> classes. A <b>PropertyItem</b> object holds one piece of image metadata.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">PropertyItem</b> has these types of members:


## -remarks



To set a property item (piece of metadata), pass the address of a <b>PropertyItem</b> object to the <a href="https://msdn.microsoft.com/20201f1e-fa80-4a7b-b7cc-7737d4a434a5">Image::SetPropertyItem</a> method of an 
				<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object. To retrieve a property item, pass the address of a <b>PropertyItem</b> object to the <a href="https://msdn.microsoft.com/ca96c4a3-058f-4ba4-a8be-2692ecd76710">Image::GetPropertyItem</a> method of an 
				<b>Image</b> object.




## -see-also




<a href="https://msdn.microsoft.com/c22c2027-9552-4f35-ba44-755d872ceea7">Image::GetAllPropertyItems</a>



<a href="https://msdn.microsoft.com/2318eb42-9006-4361-ac5c-4e5325dc4947">Image::GetPropertyIdList</a>



<a href="https://msdn.microsoft.com/ca96c4a3-058f-4ba4-a8be-2692ecd76710">Image::GetPropertyItem</a>



<a href="https://msdn.microsoft.com/574d3d5b-2440-4ab4-9d90-75282ea0f10d">Image::GetPropertyItemSize</a>



<a href="https://msdn.microsoft.com/731c0d1a-1918-4db8-ace1-e8a42cdefa3d">Image::GetPropertySize</a>



<a href="https://msdn.microsoft.com/ad849843-80e7-4773-96b0-f50dbdbfd61b">Image::RemovePropertyItem</a>



<a href="https://msdn.microsoft.com/20201f1e-fa80-4a7b-b7cc-7737d4a434a5">Image::SetPropertyItem</a>



<a href="https://msdn.microsoft.com/2febea35-3fea-4a2d-baaf-7a4f935fc81f">Reading and Writing Metadata</a>
 

 

