---
UID: NF:d2d1helper.BezierSegment
title: BezierSegment function
author: windows-sdk-content
description: Creates a D2D1_BEZIER_SEGMENT structure.
old-location: direct2d\beziersegment.htm
tech.root: direct2d
ms.assetid: 50938354-f9b7-40a9-807d-708f6a065912
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: BezierSegment, BezierSegment function [Direct2D], d2d1helper/BezierSegment, direct2d.beziersegment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1helper.h
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
 - BezierSegment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BezierSegment function


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/Dd368070(v=VS.85).aspx">D2D1_BEZIER_SEGMENT</a> structure.


## -parameters




### -param point1 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The first control point for the Bezier segment.


### -param point2 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The second control point for the Bezier segment.




### -param point3 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Dd368140(v=VS.85).aspx">D2D1_POINT_2F</a></b>

The end point for the Bezier segment.




## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd368070(v=VS.85).aspx">D2D1_BEZIER_SEGMENT</a></b>

The new Bezier segment.




## -see-also




<a href="https://msdn.microsoft.com/6d2c1959-1309-45d8-8204-19ffea03375b">ID2D1GeometrySink</a>
 

 

