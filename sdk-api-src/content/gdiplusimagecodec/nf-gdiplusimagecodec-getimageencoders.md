---
UID: NF:gdiplusimagecodec.GetImageEncoders
title: GetImageEncoders function
author: windows-sdk-content
description: The GetImageEncoders function gets an array of ImageCodecInfo objects that contain information about the available image encoders.
old-location: gdiplus\_gdiplus_FUNC_GetImageEncoders_numEncoders_size_encoders_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimageencoders.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetImageEncoders, GetImageEncoders function [GDI+], _gdiplus_FUNC_GetImageEncoders_numEncoders_size_encoders_, gdiplus._gdiplus_FUNC_GetImageEncoders_numEncoders_size_encoders_, gdiplusimagecodec/GetImageEncoders
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - GetImageEncoders
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# GetImageEncoders function


## -description


The <b>GetImageEncoders</b> function gets an array of 
			<a href="https://msdn.microsoft.com/en-us/library/ms534466(v=VS.85).aspx">ImageCodecInfo</a> objects that contain information about the available image encoders.


## -parameters




### -param numEncoders [in]

Type: <b>UINT</b>

Integer that specifies the number of available image encoders. Call <a href="https://msdn.microsoft.com/en-us/library/ms534081(v=VS.85).aspx">GetImageEncodersSize</a> to determine this number. 


### -param size [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the array of 
					<a href="https://msdn.microsoft.com/en-us/library/ms534466(v=VS.85).aspx">ImageCodecInfo</a> objects. Call <a href="https://msdn.microsoft.com/en-us/library/ms534081(v=VS.85).aspx">GetImageEncodersSize</a> to determine this number. 


### -param encoders [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534466(v=VS.85).aspx">ImageCodecInfo</a>*</b>

Pointer to a buffer that receives the array of 
					<a href="https://msdn.microsoft.com/en-us/library/ms534466(v=VS.85).aspx">ImageCodecInfo</a> objects. You must allocate memory for this buffer. Call <a href="https://msdn.microsoft.com/en-us/library/ms534081(v=VS.85).aspx">GetImageEncodersSize</a> to determine the size of the required buffer. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534078(v=VS.85).aspx">GetImageDecoders</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534079(v=VS.85).aspx">GetImageDecodersSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534081(v=VS.85).aspx">GetImageEncodersSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533814(v=VS.85).aspx">Using Image Encoders and Decoders</a>
 

 

