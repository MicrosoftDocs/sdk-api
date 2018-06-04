---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

