---
UID: NF:icm.CMTranslateColors
title: CMTranslateColors function
author: windows-sdk-content
description: The CMTranslateColors function translates an array of colors from a source color space to a destination color space using a color transform.
old-location: wcs\cmtranslatecolors.htm
tech.root: WCS
ms.assetid: 5c775e36-ee45-4b8a-ac12-6219063e185a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CMTranslateColors, CMTranslateColors function [Windows Color System], _color_CMTranslateColors, icm/CMTranslateColors, wcs.cmtranslatecolors
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
 - CMTranslateColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CMTranslateColors
: 
---

# CMTranslateColors function


## -description


The <b>CMTranslateColors</b> function translates an array of colors from a source <a href="c.htm">color space</a> to a destination color space using a color transform.


## -parameters




### -param hcmTransform

Specifies the color transform to use.


### -param lpaInputColors

Points to an array of <a href="color.htm">COLOR</a> structures to translate.


### -param nColors

Specifies the number of elements in the array.


### -param ctInput

Specifies the color type of the input.


### -param lpaOutputColors

Points to a buffer in which an array of translated <b>COLOR</b> structures is to be placed.


### -param ctOutput

Specifies the output color type.


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. The CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



Every CMM is required to export this function.

If the input and the output color types are not compatible with the color transform, this function should fail.

Note that this function must support in-place translation. That is, whenever the memory footprint of the output is less than or equal to the memory footprint of the input, this function must be able to translate the bitmap colors even if the source and destination buffers are the same.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

