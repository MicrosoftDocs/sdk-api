---
UID: NS:strmif._NORMALIZEDRECT
title: "_NORMALIZEDRECT"
author: windows-sdk-content
description: The NORMALIZEDRECT structure is used with the VMR filter in mixing operations to specify the location of a video rectangle in composition space.
old-location: dshow\normalizedrect.htm
old-project: DirectShow
ms.assetid: c40a0feb-f33e-40e3-9c58-0a22d2aa1858
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: "*PNORMALIZEDRECT, NORMALIZEDRECT, NORMALIZEDRECT structure [DirectShow], NORMALIZEDRECT2, PNORMALIZEDRECT, PNORMALIZEDRECT structure pointer [DirectShow], _NORMALIZEDRECT, dshow.normalizedrect, strmif/NORMALIZEDRECT, strmif/PNORMALIZEDRECT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NORMALIZEDRECT, *PNORMALIZEDRECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - NORMALIZEDRECT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP
---

# _NORMALIZEDRECT structure


## -description


The <code>NORMALIZEDRECT</code> structure is used with the VMR filter in mixing operations to specify the location of a video rectangle in composition space.
        


## -struct-fields




### -field left

The left corner of the normalized rectangle.


### -field top

The top corner of the normalized rectangle.
          


### -field right

The right corner of the normalized rectangle.
          


### -field bottom

The bottom corner of the normalized rectangle.
          


## -remarks



This structure is used in methods involving "composition space," which refers to the visible video rectangle, as well as the offscreen space necessary to contain rectangles from secondary streams. See <a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

