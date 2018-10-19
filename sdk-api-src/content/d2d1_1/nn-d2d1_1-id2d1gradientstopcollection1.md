---
UID: NN:d2d1_1.ID2D1GradientStopCollection1
title: ID2D1GradientStopCollection1
author: windows-sdk-content
description: Represents a collection of D2D1_GRADIENT_STOP objects for linear and radial gradient brushes. It provides get methods for all the new parameters added to the gradient stop collection.
old-location: direct2d\id2d1gradientstopcollection1.htm
tech.root: direct2d
ms.assetid: aa423e18-c6b5-4587-b044-deda00a84615
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ID2D1GradientStopCollection1, ID2D1GradientStopCollection1 interface [Direct2D], ID2D1GradientStopCollection1 interface [Direct2D],described, d2d1_1/ID2D1GradientStopCollection1, direct2d.id2d1gradientstopcollection1
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
req.lib: 
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
 - ID2D1GradientStopCollection1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GradientStopCollection1 interface


## -description


Represents a collection of <a href="https://msdn.microsoft.com/f6798542-382a-4074-bbe1-707bc00b3575">D2D1_GRADIENT_STOP</a> objects for linear and radial gradient brushes. It provides get methods for all the new parameters added to the gradient stop collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GradientStopCollection1</b> interface inherits from <a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>. <b>ID2D1GradientStopCollection1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GradientStopCollection1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a59c903-0fa8-4d2c-b426-8d3c3410c6bd">GetBufferPrecision</a>
</td>
<td align="left" width="63%">
Gets the precision of the gradient buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D1351D2B-B259-400C-A77A-2437E80D46E9">GetColorInterpolationMode</a>
</td>
<td align="left" width="63%">
Retrieves the color interpolation mode that the gradient stop collection uses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da3987a5-b40f-49eb-9930-0162cf64d6a9">GetGradientStops1</a>
</td>
<td align="left" width="63%">
Copies the gradient stops from the collection into memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb579d25-f38c-4f26-a29b-c6875cbabb3b">GetPostInterpolationSpace</a>
</td>
<td align="left" width="63%">
Gets the color space after interpolation has occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8222d713-c47e-4e4c-92aa-040dc9085ce9">GetPreInterpolationSpace</a>
</td>
<td align="left" width="63%">
Gets the color space of the input colors as well as the space in which gradient stops are interpolated.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6374fc62-1f54-4112-8ba3-9c1167bf8685">ID2D1DeviceContext::CreateGradientStopCollection</a>



<a href="https://msdn.microsoft.com/982abf9c-4778-4871-a494-5843f0c0addc">ID2D1GradientStopCollection</a>



<a href="https://msdn.microsoft.com/674ffba5-18c5-46bf-8813-d8d13e5ba903">ID2D1RenderTarget::CreateGradientStopCollection</a>
 

 

