---
UID: NF:d2d1_3helper.InkBezierSegment
title: InkBezierSegment function (d2d1_3helper.h)
author: windows-sdk-content
description: Creates a D2D1_INK_BEZIER_SEGMENT structure.
old-location: direct2d\inkbeziersegment.htm
tech.root: Direct2D
ms.assetid: 61f6a6fb-3304-e979-549a-3c4c528ed12d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InkBezierSegment, InkBezierSegment function [Direct2D], d2d1_3helper/InkBezierSegment, direct2d.inkbeziersegment
ms.topic: function
f1_keywords: 
 - "d2d1_3helper/InkBezierSegment"
req.header: d2d1_3helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - InkBezierSegment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InkBezierSegment function


## -description


Creates a <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment">D2D1_INK_BEZIER_SEGMENT</a> structure.
        


## -parameters




### -param point1 [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point">D2D1_INK_POINT</a></b>

The first control point for the Bezier segment.


### -param point2 [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point">D2D1_INK_POINT</a></b>

The second control point for the Bezier segment.


### -param point3 [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point">D2D1_INK_POINT</a></b>

The end point for the Bezier segment.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment">D2D1_INK_BEZIER_SEGMENT</a></b>

Returns the created <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment">D2D1_INK_BEZIER_SEGMENT</a> structure.
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment">D2D1_INK_BEZIER_SEGMENT</a>
 

 

