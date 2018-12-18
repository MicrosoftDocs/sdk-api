---
UID: NN:d2d1effectauthor.ID2D1SourceTransform
title: ID2D1SourceTransform
author: windows-sdk-content
description: Represents a CPU-based rasterization stage in the transform pipeline graph.
old-location: direct2d\id2d1sourcetransform.htm
tech.root: direct2d
ms.assetid: A2B3E8E1-8F7F-4AFA-B1CE-5E8A5FCD9B70
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1SourceTransform, ID2D1SourceTransform interface [Direct2D], ID2D1SourceTransform interface [Direct2D],described, d2d1effectauthor/ID2D1SourceTransform, direct2d.id2d1sourcetransform
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
 - ID2D1SourceTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SourceTransform interface


## -description


Represents a CPU-based rasterization stage in the transform  pipeline graph.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SourceTransform</b> interface inherits from <a href="https://msdn.microsoft.com/8A0CD795-A6D8-4817-9676-58C11DDAAEBD">ID2D1Transform</a>. <b>ID2D1SourceTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SourceTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38EBBFB2-7A49-4386-80B3-86B44BF2FC39">Draw</a>
</td>
<td align="left" width="63%">
Draws the transform to the GPU–based Direct2D pipeline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7082A748-E1DF-4805-BBB5-9EF50841B36D">SetRenderInfo</a>
</td>
<td align="left" width="63%">
Sets the render information for the transform.

</td>
</tr>
</table> 


## -remarks



<b>ID2D1SourceTransform</b> specializes an implementation of the Shantzis calculations to a transform implemented as the source of an effect graph with the data being provided from sytem memory.




## -see-also




<a href="https://msdn.microsoft.com/8A0CD795-A6D8-4817-9676-58C11DDAAEBD">ID2D1Transform</a>
 

 

