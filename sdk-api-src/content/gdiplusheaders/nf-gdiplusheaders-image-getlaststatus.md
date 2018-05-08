---
UID: NF:gdiplusheaders.Image.GetLastStatus
title: Image::GetLastStatus
author: windows-driver-content
description: The Image::GetLastStatus method returns a value that indicates the nature of this Image object's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_Image_GetLastStatus_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getlaststatus_65.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],Image class, Image class [GDI+],GetLastStatus method, Image.GetLastStatus, Image::GetLastStatus, _gdiplus_CLASS_Image_GetLastStatus_, gdiplus._gdiplus_CLASS_Image_GetLastStatus_
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	Image.GetLastStatus
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Image::GetLastStatus


## -description


The <b>Image::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

The <b>Image::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If no methods invoked on this 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object have failed since the previous call to <b>Image::GetLastStatus</b>, then <b>Image::GetLastStatus</b> returns Ok.

If at least one method invoked on this 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object has failed since the previous call to <b>Image::GetLastStatus</b>, then <b>Image::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>Image::GetLastStatus</b> immediately after constructing an 
				<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object to determine whether the constructor succeeded.

The first time you call the <b>Image::GetLastStatus</b> method of an 
				<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the 
				<b>Image</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/ddde257c-41a6-4f6e-8d81-10d66c60085c">Images, Bitmaps, and Metafiles</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>



<a href="https://msdn.microsoft.com/57e3bf33-5490-4f4a-addf-356ef8f1aeed">Using Images, Bitmaps, and Metafiles</a>
 

 

