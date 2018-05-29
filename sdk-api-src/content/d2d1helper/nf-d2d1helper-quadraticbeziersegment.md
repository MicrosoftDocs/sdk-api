---
UID: NF:d2d1helper.QuadraticBezierSegment
title: QuadraticBezierSegment function
author: windows-sdk-content
description: Creates a D2D1_QUADRATIC_BEZIER_SEGMENT structure.
old-location: direct2d\quadraticbeziersegment.htm
old-project: Direct2D
ms.assetid: 9b72e367-85dd-4a1f-a67e-34fc4b078ebe
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: QuadraticBezierSegment, QuadraticBezierSegment function [Direct2D], d2d1helper/QuadraticBezierSegment, direct2d.quadraticbeziersegment
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1helper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D2D1_VIGNETTE_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D2d1.dll
api_name:
-	QuadraticBezierSegment
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# QuadraticBezierSegment function


## -description


Creates a <a href="https://msdn.microsoft.com/5060cb17-b6f4-4796-b91d-602fd81591c2">D2D1_QUADRATIC_BEZIER_SEGMENT</a> structure.


## -parameters




### -param point1 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The control point of the quadratic Bezier segment.


### -param point2 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/b317ae75-d738-4e1a-bcd1-adf3e95b197e">D2D1_POINT_2F</a></b>

The end point of the quadratic Bezier segment.


## -returns



Type: <b><a href="https://msdn.microsoft.com/5060cb17-b6f4-4796-b91d-602fd81591c2">D2D1_QUADRATIC_BEZIER_SEGMENT</a></b>

The new quadratic Bezier curve segment.



