---
UID: NF:gdiplusheaders.Image.GetPhysicalDimension
title: Image::GetPhysicalDimension (gdiplusheaders.h)
author: windows-sdk-content
description: The Image::GetPhysicalDimension method gets the width and height of this image.
old-location: gdiplus\_gdiplus_CLASS_Image_GetPhysicalDimension_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getphysicaldimension.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPhysicalDimension, GetPhysicalDimension method [GDI+], GetPhysicalDimension method [GDI+],Image class, Image class [GDI+],GetPhysicalDimension method, Image.GetPhysicalDimension, Image::GetPhysicalDimension, _gdiplus_CLASS_Image_GetPhysicalDimension_size_, gdiplus._gdiplus_CLASS_Image_GetPhysicalDimension_size_
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.GetPhysicalDimension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::GetPhysicalDimension


## -description


The <b>Image::GetPhysicalDimension</b> method gets the width and height of this image.


## -parameters




### -param size [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534506(v=VS.85).aspx">SizeF</a> object that receives the width and height of this image. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536386(v=VS.85).aspx">Cropping and Scaling Images</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535373(v=VS.85).aspx">Image::GetBounds</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535380(v=VS.85).aspx">Image::GetHeight</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535381(v=VS.85).aspx">Image::GetHorizontalResolution</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535396(v=VS.85).aspx">Image::GetVerticalResolution</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535397(v=VS.85).aspx">Image::GetWidth</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533829(v=VS.85).aspx">Improving Performance by Avoiding Automatic Scaling</a>
 

 

