---
UID: NF:gdiplusimagecodec.GetImageEncodersSize
title: GetImageEncodersSize function
author: windows-sdk-content
description: The GetImageEncodersSize function gets the number of available image encoders and the total size of the array of ImageCodecInfo objects that is returned by the GetImageEncoders function.
old-location: gdiplus\_gdiplus_FUNC_GetImageEncodersSize_numEncoders_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimageencoderssize.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: GetImageEncodersSize, GetImageEncodersSize function [GDI+], _gdiplus_FUNC_GetImageEncodersSize_numEncoders_size_, gdiplus._gdiplus_FUNC_GetImageEncodersSize_numEncoders_size_, gdiplusimagecodec/GetImageEncodersSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gdiplusimagecodec.h
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
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - GetImageEncodersSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GetImageEncodersSize function


## -description


The <b>GetImageEncodersSize</b> function gets the number of available image encoders and the total size of the array of 
			<a href="https://msdn.microsoft.com/en-us/library/ms534466(v=VS.85).aspx">ImageCodecInfo</a> objects that is returned by the <a href="https://msdn.microsoft.com/en-us/library/ms534080(v=VS.85).aspx">GetImageEncoders</a> function.


## -parameters




### -param numEncoders [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the number of available image encoders. 


### -param size [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the total size, in bytes, of the array of 
					<a href="https://msdn.microsoft.com/en-us/library/ms534466(v=VS.85).aspx">ImageCodecInfo</a> objects that is returned by <a href="https://msdn.microsoft.com/en-us/library/ms534080(v=VS.85).aspx">GetImageEncoders</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534078(v=VS.85).aspx">GetImageDecoders</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534079(v=VS.85).aspx">GetImageDecodersSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534080(v=VS.85).aspx">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533814(v=VS.85).aspx">Using Image Encoders and Decoders</a>
 

 

