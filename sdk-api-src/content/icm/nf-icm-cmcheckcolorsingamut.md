---
UID: NF:icm.CMCheckColorsInGamut
title: CMCheckColorsInGamut function
author: windows-sdk-content
description: CMCheckColorsInGamut is no longer available for use as of Windows Vista.
old-location: wcs\cmcheckcolorsingamut.htm
tech.root: WCS
ms.assetid: bd650692-e8ce-4c9b-b2d7-3449c459e223
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CMCheckColorsInGamut, CMCheckColorsInGamut function [Windows Color System], _color_CMCheckColorsInGamut, icm/CMCheckColorsInGamut, wcs.cmcheckcolorsingamut
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
 - CMCheckColorsInGamut
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CMCheckColorsInGamut
: 
---

# CMCheckColorsInGamut function


## -description


<p class="CCE_Message">[<b>CMCheckColorsInGamut</b> is no longer available for use as of Windows Vista.]

Determines whether specified RGB triples lie in the output <a href="g.htm">gamut</a> of a specified transform.


## -parameters




### -param hcmTransform

Specifies the transform to use.


### -param lpaRGBTriple

Points to an array of RGB triples to check.


### -param lpaResult

Points to the buffer in which to put results.

The results are represented by an array of bytes. Each byte in the array corresponds to an RGB triple and has an unsigned value between 0 and 255. The value 0 denotes that the color is in gamut, while a nonzero value denotes that it is out of gamut. For any integer <i>n</i> in the range 0 &lt; <i>n</i> &lt; 255, a result value of <i>n</i> + 1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of <i>n</i>.


### -param nCount

Specifies the number of elements in the array.


## -returns



Beginning with Windows Vista, the default CMM (Icm32.dll) will return <b>FALSE</b> and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will report ERROR_NOT_SUPPORTED.

<b>Windows Server 2003, Windows XP and Windows 2000:  </b>If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. Call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to retrieve the error.






## -remarks



Beginning with Windows Vista, CMM Implementors are no longer required to implement this method.

<b>Windows Server 2003, Windows XP and Windows 2000:  </b>CMM Implementors are required to implement this method.

Every CMM is required to export this function.

If the function is not successful, custom CMMs should call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to set the last error to a valid error value defined in Winerror.h.






## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

