---
UID: NF:gdiplusimagecodec.GetImageDecodersSize
title: GetImageDecodersSize function (gdiplusimagecodec.h)
author: windows-sdk-content
description: The GetImageDecodersSize function gets the number of available image decoders and the total size of the array of ImageCodecInfo objects that is returned by the GetImageDecoders function.
old-location: gdiplus\_gdiplus_FUNC_GetImageDecodersSize_numDecoders_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimagedecoderssize.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetImageDecodersSize, GetImageDecodersSize function [GDI+], _gdiplus_FUNC_GetImageDecodersSize_numDecoders_size_, gdiplus._gdiplus_FUNC_GetImageDecodersSize_numDecoders_size_, gdiplusimagecodec/GetImageDecodersSize
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
 - GetImageDecodersSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GetImageDecodersSize function


## -description


The <b>GetImageDecodersSize</b> function gets the number of available image decoders and the total size of the array of 
			<a href="https://msdn.microsoft.com/en-us/library/ms534466(v=VS.85).aspx">ImageCodecInfo</a> objects that is returned by the <a href="https://msdn.microsoft.com/en-us/library/ms534078(v=VS.85).aspx">GetImageDecoders</a> function.


## -parameters




### -param numDecoders [out]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that receives the number of available image decoders.


### -param size [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the total size, in bytes, of the array of 
					<a href="https://msdn.microsoft.com/en-us/library/ms534466(v=VS.85).aspx">ImageCodecInfo</a> objects that is returned by the <a href="https://msdn.microsoft.com/en-us/library/ms534078(v=VS.85).aspx">GetImageDecoders</a> function. 


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



<a href="https://msdn.microsoft.com/en-us/library/ms534080(v=VS.85).aspx">GetImageEncoders</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534081(v=VS.85).aspx">GetImageEncodersSize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533814(v=VS.85).aspx">Using Image Encoders and Decoders</a>
 

 

