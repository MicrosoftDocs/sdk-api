---
UID: NS:d2d1_3.D2D1_INK_BEZIER_SEGMENT
title: D2D1_INK_BEZIER_SEGMENT
author: windows-sdk-content
description: Represents a Bezier segment to be used in the creation of an ID2D1Ink object. This structure differs from D2D1_BEZIER_SEGMENT in that it is composed of D2D1_INK_POINTs, which contain a radius in addition to x- and y-coordinates.
old-location: direct2d\d2d1_ink_bezier_segment.htm
tech.root: direct2d
ms.assetid: 27F1F78B-2478-4F5D-BF56-9931E767C358
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: D2D1_INK_BEZIER_SEGMENT, D2D1_INK_BEZIER_SEGMENT structure [Direct2D], d2d1_3/D2D1_INK_BEZIER_SEGMENT, direct2d.d2d1_ink_bezier_segment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d2d1_3.h
req.include-header: 
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
 - d2d1_3.h
api_name:
 - D2D1_INK_BEZIER_SEGMENT
product: Windows
targetos: Windows
req.typenames: D2D1_INK_BEZIER_SEGMENT
req.redist: 
---

# D2D1_INK_BEZIER_SEGMENT structure


## -description


Represents a Bezier segment to be used in the creation of an <a href="https://msdn.microsoft.com/4B6DD4C2-8E91-4AEA-AFB5-21B4FD13F75A">ID2D1Ink</a> object. 
        This structure differs from <a href="https://msdn.microsoft.com/en-us/library/Dd368070(v=VS.85).aspx">D2D1_BEZIER_SEGMENT</a> in that it is composed 
        of <a href="https://msdn.microsoft.com/en-us/library/Dn890752(v=VS.85).aspx">D2D1_INK_POINT</a>s, which contain a radius in addition to x- and y-coordinates.
        


## -struct-fields




### -field point1

The first control point for the Bezier segment.


### -field point2

The second control point for the Bezier segment.


### -field point3

The end point for the Bezier segment.

