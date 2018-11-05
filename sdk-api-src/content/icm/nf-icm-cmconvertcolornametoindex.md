---
UID: NF:icm.CMConvertColorNameToIndex
title: CMConvertColorNameToIndex function
author: windows-sdk-content
description: The CMConvertColorNameToIndex function converts color names in a named color space to index numbers in a color profile.
old-location: wcs\cmconvertcolornametoindex.htm
tech.root: WCS
ms.assetid: 07d7774d-ccab-42aa-9801-2ab38435396d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CMConvertColorNameToIndex, CMConvertColorNameToIndex function [Windows Color System], _color_CMConvertColorNameToIndex, icm/CMConvertColorNameToIndex, wcs.cmconvertcolornametoindex
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
 - CMConvertColorNameToIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMConvertColorNameToIndex function


## -description


The <b>CMConvertColorNameToIndex</b> function converts color names in a named color space to index numbers in a color profile.


## -parameters




### -param hProfile

The handle to a named color profile.


### -param paColorName

Pointer to an array of color name structures.


### -param paIndex

Pointer to an array of <b>DWORDS</b> that this function fills with the indices.


### -param dwCount

The number of color names to convert.


## -returns



If this function succeeds with the conversion, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. When this occurs, the CMM should call <b>SetLastError</b> to set the last error to a valid error value defined in Winerror.h.




## -remarks



This function is required in the default CMM. It is optional for all other CMMs.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

