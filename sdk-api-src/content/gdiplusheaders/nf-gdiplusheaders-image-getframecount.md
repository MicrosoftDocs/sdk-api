---
UID: NF:gdiplusheaders.Image.GetFrameCount
title: Image::GetFrameCount (gdiplusheaders.h)
author: windows-sdk-content
description: The Image::GetFrameCount method gets the number of frames in a specified dimension of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetFrameCount_dimensionID_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getframecount.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFrameCount, GetFrameCount method [GDI+], GetFrameCount method [GDI+],Image class, Image class [GDI+],GetFrameCount method, Image.GetFrameCount, Image::GetFrameCount, _gdiplus_CLASS_Image_GetFrameCount_dimensionID_, gdiplus._gdiplus_CLASS_Image_GetFrameCount_dimensionID_
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
 - Image.GetFrameCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::GetFrameCount


## -description


The <b>Image::GetFrameCount</b> method gets the number of frames in a specified dimension of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object.


## -parameters




### -param dimensionID [in]

Type: <b>const GUID*</b>

Pointer to a 
					GUID that specifies the dimension. 
					GUIDs that identify various dimensions are defined in Gdiplusimaging.h. 


## -returns



Type: <strong>Type: <b>UINT</b>
</strong>

This method returns the number of frames in the specified dimension of this 
						<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533838(v=VS.85).aspx">Copying Individual Frames from a Multiple-Frame Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533839(v=VS.85).aspx">Creating and Saving a Multiple-Frame Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534434(v=VS.85).aspx">EncoderParameter</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535378(v=VS.85).aspx">Image::GetFrameDimensionsCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535379(v=VS.85).aspx">Image::GetFrameDimensionsList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535398(v=VS.85).aspx">Image::SaveAdd Methods</a>
 

 

