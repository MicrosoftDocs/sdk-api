---
UID: NS:winddi._CLIPLINE
title: "_CLIPLINE"
author: windows-sdk-content
description: The CLIPLINE structure gives the driver access to a portion of a line between two clip regions used for drawing.
old-location: display\clipline.htm
tech.root: display
ms.assetid: ec938519-3c0c-4664-9e9a-b7fb338920f5
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*PCLIPLINE, CLIPLINE, CLIPLINE structure [Display Devices], PCLIPLINE, PCLIPLINE structure pointer [Display Devices], _CLIPLINE, display.clipline, grstrcts_01e6e35a-79ca-4dba-866e-24306b83cb51.xml, winddi/CLIPLINE, winddi/PCLIPLINE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - CLIPLINE
product: Windows
targetos: Windows
req.typenames: CLIPLINE, *PCLIPLINE
req.redist: 
---

# _CLIPLINE structure


## -description


The CLIPLINE structure gives the driver access to a portion of a line between two <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip regions</a> used for drawing.


## -struct-fields




### -field ptfxA

Specifies a POINTFIX structure that contains the starting point of the line.


### -field ptfxB

Specifies a POINTFIX structure that contains the end point of the line.


### -field lStyleState

Is a pair of 16-bit values supplied by GDI whenever the driver calls <a href="https://msdn.microsoft.com/edc64b1e-dd3f-4b6a-858c-91c49a819b0a">PATHOBJ_bEnumClipLines</a>. These two values are packed into a LONG and specify the style offset back to the first pixel of the line segment. This is the first pixel that would be rendered if the line were not clipped. This value allows the styling for the remainder of the line to be computed. Refer to <a href="https://msdn.microsoft.com/07e72190-7c8e-471e-9851-ccc037312c5c">Styled Cosmetic Lines</a> for additional information.


### -field c

Specifies the number of RUN structures in the <b>arun</b> array.


### -field arun

Is an array of <a href="https://msdn.microsoft.com/7c53ec29-2541-40d3-95df-bf73d900a6d6">RUN</a> structures. The RUN structures describe the start and stop portions of the clip line.


## -remarks



The CLIPLINE structure is used by <a href="https://msdn.microsoft.com/edc64b1e-dd3f-4b6a-858c-91c49a819b0a">PATHOBJ_bEnumClipLines</a>. The CLIPLINE structure contains the original, unclipped control points of the line segment.

See <a href="https://msdn.microsoft.com/2054aa16-6d86-4db3-8b16-4570b0374e23">GDI Data Types</a> for a description of the POINTFIX structure.




## -see-also




<a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a>



<a href="https://msdn.microsoft.com/f75f599f-43ea-4da6-a6e3-6591cf6d69f1">GDIINFO</a>



<a href="https://msdn.microsoft.com/7c53ec29-2541-40d3-95df-bf73d900a6d6">RUN</a>
 

 

