---
UID: NF:icm.CMCreateTransformExtW
title: CMCreateTransformExtW function
author: windows-sdk-content
description: The CMCreateTransformExt ANSI function creates a color transform that maps from an input LOGCOLORSPACE to an optional target space and then to an output device, using a set of flags that define how the transform should be created.
old-location: wcs\cmcreatetransformext.htm
tech.root: WCS
ms.assetid: 95b5bc2e-c790-43e0-8457-99bbbde5ecd2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CMCreateTransformExt, CMCreateTransformExt function [Windows Color System], CMCreateTransformExtW, _color_CMCreateTransformExt, icm/CMCreateTransformExt, icm/CMCreateTransformExtW, wcs.cmcreatetransformext
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
req.unicode-ansi: CMCreateTransformExtW (Unicode)
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
 - CMCreateTransformExt
 - CMCreateTransformExtW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMCreateTransformExtW function


## -description


The <b>CMCreateTransformExt</b> ANSI function creates a color transform that maps from an input <a href="https://msdn.microsoft.com/b08aec07-6ac0-47be-8dc9-d604d94dedde">LOGCOLORSPACE</a> to an optional target space and then to an output device, using a set of flags that define how the transform should be created.


## -parameters




### -param lpColorSpace

Pointer to an input logical color space structure.


### -param lpDevCharacter

Pointer to a memory-mapped device profile.


### -param lpTargetDevCharacter

Pointer to a memory-mapped target profile.


### -param dwFlags

Specifies flags to used control creation of the transform. For details, see <a href="https://msdn.microsoft.com/f3942929-272c-4f08-98ac-a4d14d2f6ac4">CMM Transform Creation Flags</a>.


## -returns



If this function succeeds, the return value is a color transform in the range 256 to 65,535. Since only the low <b>WORD</b> of the transform is retained, valid transforms cannot exceed this range.

If this function fails, the return value is an error code having a value less than 256. When the return value is less than 256, signaling an error, the CMM should use <b>SetLastError</b> to set the last error to a valid error value as defined in Winerror.h.




## -remarks



The Unicode equivalent of <b>CMCreateTransformExt</b> is <a href="https://msdn.microsoft.com/fa041ecd-8c42-4675-9e53-dd34535a2fd3">CMCreateTransformExtW</a>.

Every CMM is required to export this function.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/fa041ecd-8c42-4675-9e53-dd34535a2fd3">CMCreateTransformExtW</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>
 

 

