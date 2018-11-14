---
UID: NF:icm.CMCheckColors
title: CMCheckColors function
author: windows-sdk-content
description: The CMCheckColors function determines whether given colors lie within the output gamut of a specified transform.
old-location: wcs\cmcheckcolors.htm
tech.root: WCS
ms.assetid: 496845e9-1868-469a-bfe4-cf2f2f9046a6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CMCheckColors, CMCheckColors function [Windows Color System], _color_CMCheckColors, icm/CMCheckColors, wcs.cmcheckcolors
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
 - CMCheckColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CMCheckColors
: 
---

# CMCheckColors function


## -description


The <b>CMCheckColors</b> function determines whether given colors lie within the output <a href="g.htm">gamut</a> of a specified transform.


## -parameters




### -param hcmTransform

Handle to the color transform to use.


### -param lpaInputColors

Pointer to an array of <a href="color.htm">COLOR</a> structures to check against the output gamut.


### -param nColors

Specifies the number of elements in the array.


### -param ctInput

Specifies the input color type.


### -param lpaResult

Pointer to a buffer in which to place an array of bytes containing the test results. Each byte in the buffer corresponds to a <b>COLOR</b> structure, and on exit has been set to an unsigned value between 0 and 255. The value 0 denotes that the color is in gamut, while a nonzero value indicates that it is out of gamut. For any integer <i>n</i> such that 0 &lt; <i>n</i> &lt; 255, a result value of <i>n</i> + 1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of <i>n</i>. These values are usually generated from the <i>gamutTag</i> in the ICC profile.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. If the function is not successful, the CMM should call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set the last error to a valid error value defined in Winerror.h.




## -remarks



Every CMM is required to export this function.

If the input color type is not compatible with the color transform <b>CMCheckColors</b> fails.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

