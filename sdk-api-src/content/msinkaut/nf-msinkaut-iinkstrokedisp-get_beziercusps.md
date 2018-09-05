---
UID: NF:msinkaut.IInkStrokeDisp.get_BezierCusps
title: IInkStrokeDisp::get_BezierCusps
author: windows-sdk-content
description: Gets an array that contains the indices of the cusps of the Bezier approximation of the stroke.
old-location: tablet\iinkstrokedisp_beziercusps.htm
old-project: tablet
ms.assetid: 9fdd007a-1c8e-4389-975c-849a67be94a1
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: 9fdd007a-1c8e-4389-975c-849a67be94a1, BezierCusps property [Tablet PC], BezierCusps property [Tablet PC],IInkStrokeDisp interface, IInkStrokeDisp interface [Tablet PC],BezierCusps property, IInkStrokeDisp.BezierCusps, IInkStrokeDisp.get_BezierCusps, IInkStrokeDisp::BezierCusps, IInkStrokeDisp::get_BezierCusps, get_BezierCusps, msinkaut/IInkStrokeDisp::BezierCusps, msinkaut/IInkStrokeDisp::get_BezierCusps, tablet.iinkstrokedisp_beziercusps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkStrokeDisp.BezierCusps
 - IInkStrokeDisp.get_BezierCusps
 - IInkStrokeDisp.get_BezierCusps
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkStrokeDisp::get_BezierCusps


## -description



Gets an array that contains the indices of the <b>cusps</b> of the Bezier approximation of the stroke.



This property is read-only.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The array of Bezier control points that the <a href="https://msdn.microsoft.com/76bb749d-76cd-4c40-add3-4065d46ed6cb">BezierPoints</a> property returns are made up of x and y values. The <b>BezierCusps</b> property refers only to the x values in this array. The y values can be retrieved by an action similar to the following below.</div>
<div> </div>
A cusp is a point on the stroke where the direction of writing changes in a discontinuous fashion. For example, if the stroke represents the capital letter "L", this property returns three cusps: two corresponding to the first and last control points on the stroke and the third representing the corner of the "L".

The following code extracts the x and y values of the Bezier cusps of an <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a>, <code>theStroke</code>, and stores them in a two-dimensional array called <code>BezierCuspValues</code>.




## -see-also




<a href="https://msdn.microsoft.com/76bb749d-76cd-4c40-add3-4065d46ed6cb">BezierPoints Property</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>
 

 

