---
UID: NN:d2d1_1.ID2D1ImageBrush
title: ID2D1ImageBrush
author: windows-sdk-content
description: Represents a brush based on an ID2D1Image.
old-location: direct2d\id2d1imagebrush.htm
tech.root: direct2d
ms.assetid: c5088ce2-5744-4061-957b-25831478a714
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ID2D1ImageBrush, ID2D1ImageBrush interface [Direct2D], ID2D1ImageBrush interface [Direct2D],described, d2d1_1/ID2D1ImageBrush, direct2d.id2d1imagebrush
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - d2d1.dll
api_name:
 - ID2D1ImageBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1ImageBrush interface


## -description


Represents a brush based on an <a href="https://msdn.microsoft.com/9f7b4546-edbe-4000-a4ce-1a69563ebf9d">ID2D1Image</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1ImageBrush</b> interface inherits from <a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>. <b>ID2D1ImageBrush</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1ImageBrush</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/272b3d4d-ff76-42fa-8765-b44b1a834dbe">GetExtendModeX</a>
</td>
<td align="left" width="63%">
Gets the extend mode of the image brush on the x-axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82ffc0f7-5ea4-4369-8116-39a0fc819303">GetExtendModeY</a>
</td>
<td align="left" width="63%">
Gets the extend mode of the image brush on the y-axis of the image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5be6722-1ef5-40a5-babb-179f91412765">GetImage</a>
</td>
<td align="left" width="63%">
Gets the image associated with the image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74f708eb-e860-4186-822f-8c5296a4b3ba">GetInterpolationMode</a>
</td>
<td align="left" width="63%">
Gets the interpolation mode of the image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b1d64b9-1384-4b34-9b36-a6f56bde5920">GetSourceRectangle</a>
</td>
<td align="left" width="63%">
Gets the rectangle that will be used as the bounds of the image when drawn as an image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ac7ee07-84da-4f0e-9fa8-2455ee1d5acc">SetExtendModeX</a>
</td>
<td align="left" width="63%">
Sets how the content inside the source rectangle in the image brush will be extended on the x-axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c71dff4-f682-4649-8e29-41bcd4b911a6">SetExtendModeY</a>
</td>
<td align="left" width="63%">
Sets the extend mode on the y-axis.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d9bfb45-ea4f-44b0-aa29-0cae86768270">SetImage</a>
</td>
<td align="left" width="63%">
Sets the image associated with the provided image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e85b5bc-3df8-4ac0-b022-0faf025ea7a5">SetInterpolationMode</a>
</td>
<td align="left" width="63%">
Sets the interpolation mode for the image brush.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be445505-585f-448b-a7eb-386e18a416b3">SetSourceRectangle</a>
</td>
<td align="left" width="63%">
Sets the source rectangle in the image brush.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b8f6ff8-ba52-4d30-9bea-3de89793c868">ID2D1Brush</a>
 

 

