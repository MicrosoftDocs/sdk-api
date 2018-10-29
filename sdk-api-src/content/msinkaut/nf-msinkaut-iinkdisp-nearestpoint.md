---
UID: NF:msinkaut.IInkDisp.NearestPoint
title: IInkDisp::NearestPoint
author: windows-sdk-content
description: Retrieves the IInkStrokeDisp within the InkDisp object that is nearest to a known point, optionally providing the index of the nearest point and the distance to the stroke from the specified point.
old-location: tablet\inkdisp_nearestpoint.htm
tech.root: tablet
ms.assetid: e9ccf201-dbc9-484f-8038-6a964d304287
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IInkDisp interface [Tablet PC],NearestPoint method, IInkDisp.NearestPoint, IInkDisp::NearestPoint, NearestPoint, NearestPoint method [Tablet PC], NearestPoint method [Tablet PC],IInkDisp interface, e9ccf201-dbc9-484f-8038-6a964d304287, msinkaut/IInkDisp::NearestPoint, tablet.inkdisp_nearestpoint
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkDisp.NearestPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkDisp::NearestPoint


## -description



Retrieves the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> within the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object that is nearest to a known point, optionally providing the index of the nearest point and the distance to the stroke from the specified point.




## -parameters




### -param X [in]

The <code>x-</code>position in ink space of the point.


### -param Y [in]

Specifies the <code>y-</code>position in ink space of the point.


### -param PointOnStroke [in, out, optional]

Optional. Retrieves the point on the line of the stroke that is closest to the specified point within the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object. For example, a value of 1.5 indicates that the point falls halfway between the first and second packets of the stroke. This parameter can be <b>NULL</b>. The default value is 0.


### -param DistanceFromPacket [in, out, optional]

Optional. Retrieves the distance between the specified point in ink space and the nearest stroke in the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object. This parameter can be <b>NULL</b>. the default value is 0.


### -param Stroke [out, retval]

When this method returns, contains the <a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp</a> that contains a point that is closest to the specified point in the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object. If more than one stroke contains a point that is the same distance from the specified point, the value of this result is arbitrary.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory operation.

</td>
</tr>
</table>
 




## -remarks



The output <i>point</i> parameter is defined as a floating-point number because the point on the line of the stroke can fall between two physical coordinate points. Use this value to split the stroke with the <a href="https://msdn.microsoft.com/1ae627e9-c546-485a-880c-e59d2191884d">Split</a> method, or round the value up or down to index a packet in the stroke.

The <i>distanceFromPacket</i> parameter describes the distance from the point to the envelope of the stroke. This is the distance between the two points minus half the width of the stroke.




## -see-also




<a href="https://msdn.microsoft.com/85B683AA-D859-4717-8C61-C0EB4BBA5F61">IInkDisp</a>



<a href="https://msdn.microsoft.com/b18464ba-feb6-4bb5-9fcf-82feff9bcce4">IInkStrokeDisp Interface</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/87c01f9d-b48a-459c-99f8-9634e1693fa0">NearestPoint Method [IInkStrokeDisp Interface]</a>



<a href="https://msdn.microsoft.com/1ae627e9-c546-485a-880c-e59d2191884d">Split Method</a>
 

 

