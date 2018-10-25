---
UID: NN:d2d1.ID2D1LinearGradientBrush
title: ID2D1LinearGradientBrush
author: windows-sdk-content
description: Paints an area with a linear gradient.
old-location: direct2d\ID2D1LinearGradientBrush.htm
tech.root: direct2d
ms.assetid: bbb5e36a-d13d-448e-8686-d14ee99b1ccb
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ID2D1LinearGradientBrush, ID2D1LinearGradientBrush interface [Direct2D], ID2D1LinearGradientBrush interface [Direct2D],described, d2d1/ID2D1LinearGradientBrush, direct2d.ID2D1LinearGradientBrush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1.h
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
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1LinearGradientBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1LinearGradientBrush interface


## -description


Paints an area with a linear gradient. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1LinearGradientBrush</b> interface inherits from <a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>. <b>ID2D1LinearGradientBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1LinearGradientBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4d2f490-7712-4c37-8054-38f6bc557563">GetEndPoint</a>
</td>
<td align="left" width="63%">
Retrieves the ending coordinates of the linear gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2433d8ed-112e-4620-b207-42bf9e084e23">GetGradientStopCollection</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a> associated with this linear gradient brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b79b265-4bf4-48e7-99c9-64a52d8cb6d0">GetStartPoint</a>
</td>
<td align="left" width="63%">
Retrieves the starting coordinates of the linear gradient.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4d64f42-6038-442e-8666-0555a3e4ed75">SetEndPoint</a>
</td>
<td align="left" width="63%">
Sets the ending coordinates of the linear gradient in the brush's coordinate space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f70ab519-f64f-4c33-8239-83e093560418">SetStartPoint</a>
</td>
<td align="left" width="63%">
Sets the starting coordinates of the linear gradient in the brush's coordinate space. 

</td>
</tr>
</table> 


## -remarks



An <b>ID2D1LinearGradientBrush</b> paints an area with a linear gradient along a line between the brush start point and end   point. The gradient, defined by the brush <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>, is extruded perpendicular to this line, and then transformed by a brush transform (if specified).  

The start point and end   point are described in the brush space and are mappped to the render target when the brush is used. Note the starting and ending coordinates are absolute, not relative to the render target size. A value of (0, 0) maps to the upper-left corner of the render target, while a value of (1, 1) maps one pixel diagonally away from (0, 0). If there is a nonidentity brush transform or render target transform, the brush start point and end point are also transformed.  

It is possible to specify a gradient axis that does not completely fill the area that is being painted. When this occurs, the <a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE</a>, specified by the   <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>, determines how the remaining area is painted. 


<h3><a id="Creating_ID2D1LinearGradientBrush_Objects"></a><a id="creating_id2d1lineargradientbrush_objects"></a><a id="CREATING_ID2D1LINEARGRADIENTBRUSH_OBJECTS"></a>Creating ID2D1LinearGradientBrush Objects</h3>
To create a linear gradient brush, use the <a href="direct2d.ID2D1RenderTarget_CreateLinearGradientBrush_ptr_D2D1_LINEAR_GRADIENT_BRUSH_PROPERTIES_ptr_D2D1_BRUSH_PROPERTIES_ptr_ID2D1GradientStopCollection_ptr_ptr_ID2D1LinearGradientBrush">ID2D1RenderTarget::CreateLinearGradientBrush</a> method of the render target on which the brush will be used. The brush can only be used with the render target that created it or with  the compatible targets for that render target.

A linear gradient brush is a device-dependent resource: your application should create linear gradient brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated. (For more information about resources, see <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.)




## -see-also




<a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>
 

 

