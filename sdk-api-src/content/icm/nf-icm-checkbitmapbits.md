---
UID: NF:icm.CheckBitmapBits
title: CheckBitmapBits function
author: windows-sdk-content
description: The CheckBitmapBits function checks whether the pixels in a specified bitmap lie within the output gamut of a specified transform.
old-location: wcs\checkbitmapbits.htm
tech.root: WCS
ms.assetid: c5e13ed4-71c8-4c9c-9206-406732a7669e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CheckBitmapBits, CheckBitmapBits function [Windows Color System], _color_CheckBitmapBits, icm/CheckBitmapBits, wcs.checkbitmapbits
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
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mscms.dll
api_name:
 - CheckBitmapBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CheckBitmapBits function


## -description


The <b>CheckBitmapBits</b> function checks whether the pixels in a specified bitmap lie within the output <a href="g.htm">gamut</a> of a specified transform.


## -parameters




### -param hColorTransform

Handle to the color transform to use.


### -param pSrcBits

Pointer to the bitmap to check against the output gamut.


### -param bmInput

Specifies the format of the bitmap. Must be set to one of the values of the <a href="https://msdn.microsoft.com/2388f1b7-af70-4058-a145-abb13159766c">BMFORMAT</a> enumerated type.


### -param dwWidth

Specifies the number of pixels per scan line of the bitmap.


### -param dwHeight

Specifies the number of scan lines of the bitmap.


### -param dwStride

Specifies the number of bytes from the beginning one scan line to the beginning of the next one. If set to zero, the bitmap scan lines are assumed to be padded so as to be <b>DWORD</b>-aligned.


### -param paResult

Pointer to an array of bytes where the test results are to be placed. This results buffer must contain at least as many bytes as there are pixels in the bitmap.


### -param pfnCallback

Pointer to a callback function called periodically by <b>CheckBitmapBits</b> to report progress and allow the calling process to cancel the bitmap test. (See <a href="https://msdn.microsoft.com/4e0bfa4c-f0eb-4776-98d6-90d9adf71bee">ICMProgressProcCallback</a> )


### -param lpCallbackData

Data passed back to the callback function, for example, to identify the bitmap test about which progress is being reported.


## -returns



If this function succeeds, the return value is a nonzero value.

If this function fails, the return value is zero. For extended error information, call <b>GetLastError</b>.




## -remarks



If the input format is not compatible with the color transform, the <b>CheckBitmapBits</b> function fails.

This function places results of the tests in the buffer pointed to by <i>paResult</i>. Each byte in the buffer corresponds to a pixel in the bitmap, and has an unsigned value between 0 and 255. The value 0 denotes that the color is in gamut, while a nonzero value denotes that it is out of gamut. For any integer <i>n</i> such that 0 &lt;<i>n</i> &lt; 255, a result value of <i>n</i> + 1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of <i>n</i>.

When either of the floating point BMFORMATs, BM_32b_scARGB or BM_32b_scRGB is used, the color data being checked should not contain NaN or infinity. NaN and infinity are not considered to represent legitimate color component values, and the result of checking pixels containing NaN or infinity is meaningless in color terms. NaN or infinity values in the color data being processed will be handled silently, and an error will not be returned.

The out-of-gamut information in the gamut tags created in WCS use the perceptual color distance in CIECAM02, which is the mean square root in CIECAM02 Jab space. The distance in the legacy ICC profile gamut tags is the mean square root in CIELAB space. We recommend that you use the CIECAM02 space when it is available because it provides more perceptually accurate distance metrics.




## -see-also




<a href="https://msdn.microsoft.com/2388f1b7-af70-4058-a145-abb13159766c">BMFORMAT</a>



<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/4e0bfa4c-f0eb-4776-98d6-90d9adf71bee">ICMProgressProcCallback</a>
 

 

