---
UID: NF:gdiplusheaders.Image.GetRawFormat
title: Image::GetRawFormat
author: windows-sdk-content
description: The Image::GetRawFormat method gets a globally unique identifier ( GUID) that identifies the format of this Image object. GUIDs that identify various file formats are defined in Gdiplusimaging.h.
old-location: gdiplus\_gdiplus_CLASS_Image_GetRawFormat_format_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getrawformat.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRawFormat, GetRawFormat method [GDI+], GetRawFormat method [GDI+],Image class, Image class [GDI+],GetRawFormat method, Image.GetRawFormat, Image::GetRawFormat, _gdiplus_CLASS_Image_GetRawFormat_format_, gdiplus._gdiplus_CLASS_Image_GetRawFormat_format_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Image.GetRawFormat
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Image::GetRawFormat


## -description


The <b>Image::GetRawFormat</b> method gets a globally unique identifier (			GUID) that identifies the format of this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object. 
			GUIDs that identify various file formats are defined in Gdiplusimaging.h.


## -parameters




### -param format [out]

Type: <b>GUID*</b>

Pointer to a 
					GUID that receives the format identifier. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/2a0a73b1-692e-414a-919e-92f4b141d3d0">Image::GetType</a>



<a href="https://msdn.microsoft.com/953b3b7e-14c8-40e8-bcad-f14ccd4b260c">ImageType</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

