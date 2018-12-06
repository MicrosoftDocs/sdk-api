---
UID: NF:gdiplusheaders.Image.GetFrameCount
title: Image::GetFrameCount
author: windows-sdk-content
description: The Image::GetFrameCount method gets the number of frames in a specified dimension of this Image object.
old-location: gdiplus\_gdiplus_CLASS_Image_GetFrameCount_dimensionID_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getframecount.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFrameCount, GetFrameCount method [GDI+], GetFrameCount method [GDI+],Image class, Image class [GDI+],GetFrameCount method, Image.GetFrameCount, Image::GetFrameCount, _gdiplus_CLASS_Image_GetFrameCount_dimensionID_, gdiplus._gdiplus_CLASS_Image_GetFrameCount_dimensionID_
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
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.


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
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object.




## -see-also




<a href="https://msdn.microsoft.com/dfed0b61-2230-4911-a642-0a6e4beb08d6">Copying Individual Frames from a Multiple-Frame Image</a>



<a href="https://msdn.microsoft.com/9b61e01d-0a98-4ac3-865e-7570ed0c3cde">Creating and Saving a Multiple-Frame Image</a>



<a href="https://msdn.microsoft.com/1ea22bdc-c519-466e-ad39-192910785f4b">EncoderParameter</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/0d16501c-eedd-4cd4-85f3-f6c150b01af9">Image::GetFrameDimensionsCount</a>



<a href="https://msdn.microsoft.com/8199230e-85e9-4974-809a-32dc408d9b87">Image::GetFrameDimensionsList</a>



<a href="https://msdn.microsoft.com/e597f6e6-6e07-4afb-8905-26e4af961685">Image::SaveAdd Methods</a>
 

 

