---
UID: NF:icm.CheckColors
title: CheckColors function
author: windows-sdk-content
description: The CheckColors function determines whether the colors in an array lie within the output gamut of a specified transform.
old-location: wcs\checkcolors.htm
tech.root: WCS
ms.assetid: 405b0d35-e15f-4b1d-b5de-619432a5c65b
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CheckColors, CheckColors function [Windows Color System], _color_CheckColors, icm/CheckColors, wcs.checkcolors
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
 - CheckColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CheckColors function


## -description


The <b>CheckColors</b> function determines whether the colors in an array lie within the output <a href="g.htm">gamut</a> of a specified transform.


## -parameters




### -param hColorTransform

Handle to the color transform to use.


### -param paInputColors

Pointer to an array of <i>nColors</i> <a href="color.htm">COLOR</a> structures to translate.


### -param nColors

Contains the number of elements in the arrays pointed to by <i>paInputColors</i> and <i>paResult</i>.


### -param ctInput

Specifies the input color type.


### -param paResult

Pointer to an array of <i>nColors</i> bytes that receives the results of the test.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the input color type is not compatible with the color transform, <b>CheckColors</b> fails.

The function places results of the tests in the array pointed to by <i>paResult</i>. Each byte in the array corresponds to a <b>COLOR</b> element in the array pointed to by <i>paInputColors</i> and has an unsigned value between 0 and 255. The value 0 denotes that the color is in gamut, while a nonzero value denotes that it is out of gamut. For any integer <i>n</i> such that 0 &lt; <i>n</i> &lt; 255, a result value of <i>n</i> +1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of <i>n</i>.

The out-of-gamut information in the gamut tags created in WCS use the perceptual color distance in CIECAM02, which is the mean square root in CIECAM02 Jab space. The distance in the legacy ICC profile gamut tags is the mean square root in CIELAB space. We recommend that you use the CIECAM02 space when it is available because it provides more perceptually accurate distance metrics.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="color.htm">The COLOR Structure</a>
 

 

