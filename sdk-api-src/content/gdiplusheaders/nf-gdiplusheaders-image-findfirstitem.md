---
UID: NF:gdiplusheaders.Image.FindFirstItem
title: Image::FindFirstItem
author: windows-sdk-content
description: The Image::FindFirstItem method retrieves the description and the data size of the first metadata item in this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_FindFirstItem_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\findfirstitem.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: FindFirstItem, FindFirstItem method [GDI+], FindFirstItem method [GDI+],Image class, Image class [GDI+],FindFirstItem method, Image.FindFirstItem, Image::FindFirstItem, _gdiplus_CLASS_Image_FindFirstItem_, gdiplus._gdiplus_CLASS_Image_FindFirstItem_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - Image.FindFirstItem
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.1
---

# Image::FindFirstItem


## -description


The <b>Image::FindFirstItem</b> method retrieves the description and the data size of the first metadata item in this <a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a> object.


## -parameters




### -param item [in, out]

Type: <b><a href="https://msdn.microsoft.com/library/ms534468(v=VS.85).aspx">ImageItemData</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/library/ms534468(v=VS.85).aspx">ImageItemData</a> object. On input, the Desc member points to a buffer (allocated by the caller) large enough to hold the metadata description (1 byte for JPEG, 4 bytes for PNG, 11 bytes for GIF), and the DescSize member specifies the size (1, 4, or 6) of the buffer pointed to by Desc. On output, the buffer pointed to by Desc receives the metadata description, and the DataSize member receives the size, in bytes, of the metadata itself. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



Use <b>Image::FindFirstItem</b> along with <a href="https://msdn.microsoft.com/library/ms535369(v=VS.85).aspx">Image::FindNextItem</a> to enumerate the metadata items, including custom metadata, stored in an image. <b>Image::FindFirstItem</b> and <b>Image::FindNextItem</b> do not enumerate the metadata items stored by the <a href="https://msdn.microsoft.com/library/ms535405(v=VS.85).aspx">Image::SetPropertyItem</a> method.




## -see-also




<a href="https://msdn.microsoft.com/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/library/ms535382(v=VS.85).aspx">Image::GetItemData</a>
 

 

