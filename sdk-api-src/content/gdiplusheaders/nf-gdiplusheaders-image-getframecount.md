---
UID: NF:gdiplusheaders.Image.GetFrameCount
title: Image::GetFrameCount (gdiplusheaders.h)
author: windows-sdk-content
description: The Image::GetFrameCount method gets the number of frames in a specified dimension of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetFrameCount_dimensionID_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getframecount.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# Image::GetFrameCount


## -description


The <b>Image::GetFrameCount</b> method gets the number of frames in a specified dimension of this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.


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
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use">Copying Individual Frames from a Multiple-Frame Image</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-creating-and-saving-a-multiple-frame-image-use">Creating and Saving a Multiple-Frame Image</a>



<a href="https://docs.microsoft.com/previous-versions//ms534434(v=vs.85)">EncoderParameter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getframedimensionscount">Image::GetFrameDimensionsCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getframedimensionslist">Image::GetFrameDimensionsList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)">Image::SaveAdd Methods</a>
 

 

