---
UID: NF:icm.CMTranslateRGBsExt
title: CMTranslateRGBsExt function
author: windows-sdk-content
description: The CMTranslateRGBsExt function translates a bitmap from one defined format into a different defined format and calls a callback function periodically, if one is specified, to report progress and permit the calling application to terminate the translation.
old-location: wcs\cmtranslatergbsext.htm
tech.root: WCS
ms.assetid: 521d39b3-0060-469c-808a-8d443d8f9d89
ms.author: windowssdkdev
ms.date: 10/03/2018
ms.keywords: CMTranslateRGBsExt, CMTranslateRGBsExt function [Windows Color System], _color_CMTranslateRGBsExt, icm/CMTranslateRGBsExt, wcs.cmtranslatergbsext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Gdi32.lib
req.dll: Icm32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - icm32.dll
api_name:
 - CMTranslateRGBsExt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMTranslateRGBsExt function


## -description


The <b>CMTranslateRGBsExt</b> function translates a bitmap from one defined format into a different defined format and calls a callback function periodically, if one is specified, to report progress and permit the calling application to terminate the translation.


## -parameters




### -param hcmTransform

Specifies the color transform to use.


### -param lpSrcBits

Pointer to the bitmap to translate.


### -param bmInput

Specifies the input bitmap format.


### -param dwWidth

Specifies the number of pixels per scan line in the input bitmap.


### -param dwHeight

Specifies the number of scan lines in the input bitmap.


### -param dwInputStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the input bitmap. If <i>dwInputStride</i> is set to zero, the CMM should assume that scan lines are padded so as to be <b>DWORD</b>-aligned.


### -param lpDestBits

Points to a destination buffer in which to place the translated bitmap.


### -param bmOutput

Specifies the output bitmap format.


### -param dwOutputStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the input bitmap. If <i>dwOutputStride</i> is set to zero, the CMM should pad scan lines so that they are <b>DWORD</b>-aligned.


### -param lpfnCallback

Pointer to an application-supplied callback function called periodically by <b>CMTranslateRGBsExt</b> to report progress and allow the calling process to cancel the translation. (See <a href="https://msdn.microsoft.com/4e0bfa4c-f0eb-4776-98d6-90d9adf71bee">ICMProgressProcCallback</a>.)


### -param ulCallbackData

Data passed back to the callback function, for example to identify the translation that is reporting progress.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b> and the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



Every CMM is required to export this function.

When writing into the destination buffer, the CMM should make sure that scan lines are padded to be <b>DWORD</b>-aligned.

If the input and output formats are not compatible with the color transform, this function fails.

If both input and output bitmap formats are 3 channel, 4 bytes per pixel as in the case of BM_xRGBQUADS, the fourth bytes should be preserved and copied to the output buffer.

If the callback function returns zero, processing should be cancelled and <b>CMTranslateRGBsExt</b> should return zero to indicate failure; the output buffer may be partially filled.

Note that this function must support in-place translation. That is, whenever the memory footprint of the output is less than or equal to the memory footprint of the input, this function must be able to translate the bitmap colors even if the source and destination buffers are the same.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/4e0bfa4c-f0eb-4776-98d6-90d9adf71bee">ICMProgressProcCallback</a>



<a href="using_structures_in_wcs_1_0.htm">Windows Bitmap Header Structures</a>
 

 

