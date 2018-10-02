---
UID: NF:icm.ConvertIndexToColorName
title: ConvertIndexToColorName function
author: windows-sdk-content
description: The ConvertIndexToColorName transforms indices in a color space to an array of names in a named color space.
old-location: wcs\convertindextocolorname.htm
tech.root: WCS
ms.assetid: 9199a0f5-d2ec-4831-a5da-1835d2780f9d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ConvertIndexToColorName, ConvertIndexToColorName function [Windows Color System], _color_ConvertIndexToColorName, icm/ConvertIndexToColorName, wcs.convertindextocolorname
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
 - ConvertIndexToColorName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ConvertIndexToColorName function


## -description


The <b>ConvertIndexToColorName</b> transforms indices in a color space to an array of names in a named color space.


## -parameters




### -param hProfile

The handle to an International Color Consortium (ICC) color space profile.


### -param paIndex

Pointer to an array of color-space index numbers. The indices begin with one, not zero.


### -param paColorName

Pointer to an array of color name structures.


### -param dwCount

The number of indices to convert.


## -returns



If this conversion function succeeds, the return value is <b>TRUE</b>.

If this conversion function fails, the return value is <b>FALSE</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because named profiles are explicit ICC profile types.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

