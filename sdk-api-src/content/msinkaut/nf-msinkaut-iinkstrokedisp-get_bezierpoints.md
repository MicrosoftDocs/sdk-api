---
UID: NF:msinkaut.IInkStrokeDisp.get_BezierPoints
title: IInkStrokeDisp::get_BezierPoints method
author: windows-driver-content
description: Gets the array of control points that represent the Bezier approximation of the stroke.
old-location: tablet\iinkstrokedisp_bezierpoints.htm
old-project: tablet
ms.assetid: 76bb749d-76cd-4c40-add3-4065d46ed6cb
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: 76bb749d-76cd-4c40-add3-4065d46ed6cb, BezierPoints property [Tablet PC], BezierPoints property [Tablet PC], IInkStrokeDisp interface, IInkStrokeDisp, IInkStrokeDisp interface [Tablet PC], BezierPoints property, IInkStrokeDisp.BezierPoints, IInkStrokeDisp.get_BezierPoints, IInkStrokeDisp::get_BezierPoints, get_BezierPoints,IInkStrokeDisp.get_BezierPoints, msinkaut/IInkStrokeDisp::BezierPoints, msinkaut/IInkStrokeDisp::get_BezierPoints, tablet.iinkstrokedisp_bezierpoints
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkStrokeDisp.BezierPoints
-	IInkStrokeDisp.get_BezierPoints
-	IInkStrokeDisp.get_BezierPoints
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkStrokeDisp::get_BezierPoints method


## -description



Gets the array of control points that represent the Bezier approximation of the stroke.



This property is read-only.


## -parameters


## -remarks



The control points that the <b>BezierPoints</b> property returns provide a smooth approximation of the original stroke and do not necessarily lie on the stroke.




## -see-also




<a href="https://msdn.microsoft.com/9fdd007a-1c8e-4389-975c-849a67be94a1">BezierCusps Property</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>
 

 

