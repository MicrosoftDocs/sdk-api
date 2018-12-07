---
UID: NF:icm.CMConvertIndexToColorName
title: CMConvertIndexToColorName function
author: windows-sdk-content
description: The CMConvertIndexToColorName transforms indices in a color space to an array of names in a named color space.
old-location: wcs\cmconvertindextocolorname.htm
tech.root: WCS
ms.assetid: 47506ccf-6106-46db-b5dc-90ba34135191
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CMConvertIndexToColorName, CMConvertIndexToColorName function [Windows Color System], _color_CMConvertIndexToColorName, icm/CMConvertIndexToColorName, wcs.cmconvertindextocolorname
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
 - CMConvertIndexToColorName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CMConvertIndexToColorName
: 
---

# CMConvertIndexToColorName function


## -description


The <b>CMConvertIndexToColorName</b> transforms indices in a color space to an array of names in a named color space.


## -parameters




### -param hProfile

The handle to a color space profile.


### -param paIndex

Pointer to an array of color-space index numbers.


### -param paColorName

Pointer to an array of color name structures.


### -param dwCount

The number of indices to convert.


## -returns



If this conversion function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. When this occurs, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



This function is required in the default CMM. It is optional for all other CMMs.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

