---
UID: NF:gdiplusheaders.Image.GetPhysicalDimension
title: Image::GetPhysicalDimension
author: windows-sdk-content
description: The Image::GetPhysicalDimension method gets the width and height of this image.
old-location: gdiplus\_gdiplus_CLASS_Image_GetPhysicalDimension_size_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getphysicaldimension.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetPhysicalDimension, GetPhysicalDimension method [GDI+], GetPhysicalDimension method [GDI+],Image class, Image class [GDI+],GetPhysicalDimension method, Image.GetPhysicalDimension, Image::GetPhysicalDimension, _gdiplus_CLASS_Image_GetPhysicalDimension_size_, gdiplus._gdiplus_CLASS_Image_GetPhysicalDimension_size_
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
-	Image.GetPhysicalDimension
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Image::GetPhysicalDimension


## -description


The <b>Image::GetPhysicalDimension</b> method gets the width and height of this image.


## -parameters




### -param size [out]

Type: <b><a href="https://msdn.microsoft.com/b40ade07-f89e-44ba-9185-9aec01f1051f">SizeF</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/b40ade07-f89e-44ba-9185-9aec01f1051f">SizeF</a> object that receives the width and height of this image. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/81d20adc-0481-4b1b-80aa-ae218fdecd84">Cropping and Scaling Images</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/b94cee76-2e3d-4f78-96b3-ec898054bd6e">Image::GetBounds</a>



<a href="https://msdn.microsoft.com/a39deeae-e610-4468-ba93-1da5abaa00b8">Image::GetHeight</a>



<a href="https://msdn.microsoft.com/09e0d6d9-10b5-4319-8547-f13ca06cf0cd">Image::GetHorizontalResolution</a>



<a href="https://msdn.microsoft.com/8aa90120-479e-4fa7-b9d8-609fdf1912e7">Image::GetVerticalResolution</a>



<a href="https://msdn.microsoft.com/e55bc22d-e5c6-43c8-87f8-345d348e5707">Image::GetWidth</a>



<a href="https://msdn.microsoft.com/da571970-a4fc-4d4a-9264-0085d9807d66">Improving Performance by Avoiding Automatic Scaling</a>
 

 

