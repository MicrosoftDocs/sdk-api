---
UID: NN:d2d1effectauthor.ID2D1Transform
title: ID2D1Transform
author: windows-sdk-content
description: Represents the base interface for all of the transforms implemented by the transform author.
old-location: direct2d\id2d1transform.htm
tech.root: Direct2D
ms.assetid: 8A0CD795-A6D8-4817-9676-58C11DDAAEBD
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID2D1Transform, ID2D1Transform interface [Direct2D], ID2D1Transform interface [Direct2D],described, d2d1effectauthor/ID2D1Transform, direct2d.id2d1transform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1effectauthor.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1Transform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Transform interface


## -description


Represents the base interface for all of the transforms implemented by the transform author.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Transform</b> interface inherits from <a href="https://msdn.microsoft.com/2ACF65DA-A812-4983-B044-71103A9AA450">ID2D1TransformNode</a>. <b>ID2D1Transform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Transform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8FC15A61-767C-460A-A260-9F56A41DA87F">MapInputRectsToOutputRect</a>
</td>
<td align="left" width="63%">
Performs the inverse mapping to <a href="https://msdn.microsoft.com/EE098F67-B5A7-41C1-886A-2C7779B5E05C">MapOutputRectToInputRects</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46E6EAF3-7EC7-4433-90E5-4C6E3A56AFA5">MapInvalidRect</a>
</td>
<td align="left" width="63%">
Sets the input rectangles for this rendering pass into the transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EE098F67-B5A7-41C1-886A-2C7779B5E05C">MapOutputRectToInputRects</a>
</td>
<td align="left" width="63%">
Allows a transform to state how it would map a rectangle requested on its output to a set of sample rectangles on its input.

</td>
</tr>
</table> 


## -remarks



Transforms are aggregated by effect authors. This interface  provides a common interface for implementing the Shantzis rectangle calculations which is the basis for all the transform processing in Direct2D imaging extensions.  These  calculations are described in the paper <a href="http://dl.acm.org/citation.cfm?id=192191">A model for efficient and flexible image computing</a>.




## -see-also




<a href="https://msdn.microsoft.com/2ACF65DA-A812-4983-B044-71103A9AA450">ID2D1TransformNode</a>
 

 

