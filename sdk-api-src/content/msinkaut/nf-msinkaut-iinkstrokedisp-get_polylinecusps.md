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

# IInkStrokeDisp::get_PolylineCusps


## -description



Gets an array that contains the indices of the cusps of the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> object.



This property is read-only.


## -parameters


## -remarks



The array returned by the <b>PolylineCusps</b> property is an index into the array returned by the <a href="https://msdn.microsoft.com/76378521-15d1-48a0-ae9f-8362faf60c9f">GetPoints</a> method. Each index in the <b>PolylineCusps</b> property corresponds to a point in the array returned by the <b>GetPoints</b> method that is a cusp of the points of the stroke.

A cusp is a point on the stroke where the direction of writing changes in a discontinuous fashion. For example, if the stroke represents the capital letter "L", this property returns three cusps: two corresponding to the first and last control points on the stroke and the third representing the corner of the "L".

The location of a cusp can be determined by using the cusp as an index into the array returned by the <a href="https://msdn.microsoft.com/76378521-15d1-48a0-ae9f-8362faf60c9f">GetPoints</a> method.




## -see-also




<a href="https://msdn.microsoft.com/76378521-15d1-48a0-ae9f-8362faf60c9f">GetPoints Method</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>
 

 

