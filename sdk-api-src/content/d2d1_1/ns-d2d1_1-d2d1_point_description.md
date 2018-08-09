---
UID: NS:d2d1_1.D2D1_POINT_DESCRIPTION
title: D2D1_POINT_DESCRIPTION
author: windows-sdk-content
description: Describes a point on a path geometry.
old-location: direct2d\d2d1_point_description.htm
old-project: direct2d
ms.assetid: d6e7a4c1-135f-4ffe-91d7-486de8a9338d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_POINT_DESCRIPTION, D2D1_POINT_DESCRIPTION structure [Direct2D], PD2D1_POINT_DESCRIPTION, PD2D1_POINT_DESCRIPTION structure pointer [Direct2D], d2d1_1/D2D1_POINT_DESCRIPTION, d2d1_1/PD2D1_POINT_DESCRIPTION, direct2d.d2d1_point_description
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: D2D1.lib
tech.root: 
req.typenames: D2D1_POINT_DESCRIPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2D1.lib
api_name:
 - D2D1_POINT_DESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D2D1_POINT_DESCRIPTION structure


## -description


Describes a point on a path geometry.


## -struct-fields




### -field point

The end point after walking the path.


### -field unitTangentVector

A unit vector indicating the tangent point.


### -field endSegment

The index of the segment on which point resides. This index is global to the entire path, not just to a particular figure.


### -field endFigure

The index of the figure on which point resides.


### -field lengthToEndSegment

The length of the section of the path stretching from the start of the path  to the start of <b>endSegment</b>.


## -see-also




<a href="https://msdn.microsoft.com/4a47d928-7482-413a-ad9d-e887b309e367">ID2D1PathGeometry1::ComputePointAndSegmentAtLength</a>
 

 

