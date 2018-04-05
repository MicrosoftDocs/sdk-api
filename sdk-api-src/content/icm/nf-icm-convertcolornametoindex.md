---
UID: NF:icm.ConvertColorNameToIndex
title: ConvertColorNameToIndex function
author: windows-driver-content
description: The ConvertColorNameToIndex function converts color names in a named color space to index numbers in an International Color Consortium (ICC) color profile.
old-location: wcs\convertcolornametoindex.htm
old-project: WCS
ms.assetid: b4424cbe-0a11-419e-88d7-0aa4a57db0eb
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ConvertColorNameToIndex, ConvertColorNameToIndex function [Windows Color System], _color_ConvertColorNameToIndex, icm/ConvertColorNameToIndex, wcs.convertcolornametoindex
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
req.typenames: WCS_PROFILE_MANAGEMENT_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	mscms.dll
api_name:
-	ConvertColorNameToIndex
product: Windows
targetos: Windows
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
req.product: GDI+ 1.1
---

# ConvertColorNameToIndex function


## -description


The <b>ConvertColorNameToIndex</b> function converts color names in a named color space to index numbers in an International Color Consortium (ICC) color profile.


## -parameters




### -param hProfile

The handle to an ICC named color profile.


### -param paColorName

Pointer to an array of color name structures.


### -param paIndex

Pointer to an array of <b>DWORDS</b> that this function fills with the indices. The indices begin with one, not zero.


### -param dwCount

The number of color names to convert.


## -returns



If this function succeeds with the conversion, the return value is <b>TRUE</b>.

If the conversion function fails, the return value is <b>FALSE</b>.




## -remarks



This function will fail if <i>hProfile</i> is not a valid ICC profile.

This function does not support Windows Color System (WCS) profiles CAMP, DMP, and GMMP; because named profiles are explicit ICC profile types.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

