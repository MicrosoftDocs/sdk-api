---
UID: NF:icm.CMCheckRGBs
title: CMCheckRGBs function
author: windows-sdk-content
description: The CMCheckRGBs function checks whether the pixels in a bitmap lie within the output gamut of a specified transform.
old-location: wcs\cmcheckrgbs.htm
tech.root: WCS
ms.assetid: 1b8e33b7-0250-463b-a901-5a480205295e
ms.author: windowssdkdev
ms.date: 10/03/2018
ms.keywords: CMCheckRGBs, CMCheckRGBs function [Windows Color System], _color_CMCheckRGBs, icm/CMCheckRGBs, wcs.cmcheckrgbs
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
 - CMCheckRGBs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMCheckRGBs function


## -description


The <b>CMCheckRGBs</b> function checks whether the pixels in a bitmap lie within the output <a href="g.htm">gamut</a> of a specified transform.


## -parameters




### -param hcmTransform

Specifies the color transform to use.


### -param lpSrcBits

Points to the bitmap to check against an output gamut.


### -param bmInput

Specifies the input bitmap format.


### -param dwWidth

Specifies the number of pixels per scan line in the input bitmap.


### -param dwHeight

Specifies the number of scan lines in the input bitmap.


### -param dwStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the input bitmap. If <i>dwStride</i> is set to zero, the CMM should assume that scan lines are padded so as to be <b>DWORD-</b>aligned.


### -param lpaResult

Points to a buffer in which the test results are to be placed.

The results are represented by an array of bytes. Each byte in the array corresponds to a pixel in the bitmap, and on exit is set to an unsigned value between 0 and 255. The value 0 denotes that the color is in gamut, while a nonzero value denotes that it is out of gamut. For any integer <i>n</i> such that 0 &lt; <i>n</i> &lt; 255, a result value of <i>n</i> + 1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of n. These values are usually generated from the <i>gamutTag</i> in the ICC profile.


### -param pfnCallback

Pointer to an application-supplied callback function called periodically by <b>CMCheckRGBs</b> to report progress and allow the calling process to cancel the translation. (See <a href="https://msdn.microsoft.com/4e0bfa4c-f0eb-4776-98d6-90d9adf71bee">ICMProgressProcCallback</a>.)


### -param ulCallbackData

Data passed back to the callback function, for example to identify the bitmap test that is reporting progress.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. If the function is not successful, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



Every CMM is required to export this function.

If the input format is not compatible with the color transform, the <b>CMCheckRGBs</b> function fails.

If the callback function returns 0, processing should be canceled and <b>CMCheckRGBs</b> should return zero to indicate failure; the results buffer may be partially filled.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/4e0bfa4c-f0eb-4776-98d6-90d9adf71bee">ICMProgressProcCallback</a>
 

 

