---
UID: NN:d2d1effectauthor.ID2D1RenderInfo
title: ID2D1RenderInfo
author: windows-sdk-content
description: Describes the render information common to all of the various transform implementations.
old-location: direct2d\id2d1renderinfo.htm
tech.root: direct2d
ms.assetid: 26FB6D27-7EE0-43DA-A575-D9FF77846A16
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ID2D1RenderInfo, ID2D1RenderInfo interface [Direct2D], ID2D1RenderInfo interface [Direct2D],described, d2d1effectauthor/ID2D1RenderInfo, direct2d.id2d1renderinfo
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
 - ID2D1RenderInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderInfo interface


## -description


Describes the render information common to all of the various transform implementations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1RenderInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1RenderInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1RenderInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2325A132-5B34-48B2-90F0-2A31892E0AD8">SetCached</a>
</td>
<td align="left" width="63%">
Specifies that the output of the transform in which the render information is encapsulated is or is not cached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31571676-7030-4FBB-BDED-3CE3BA7E7CE6">SetInputDescription</a>
</td>
<td align="left" width="63%">
Sets how a specific input to the transform should be handled by the renderer in terms of sampling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44077C5C-E3AA-4AE6-B772-BF2669B205B3">SetInstructionCountHint</a>
</td>
<td align="left" width="63%">
Provides an estimated hint of shader execution cost to D2D.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4267FCA0-10AF-4731-8B68-B3425FA00185">SetOutputBuffer</a>
</td>
<td align="left" width="63%">
Allows a caller to control the output precision and channel-depth of the transform in which the render information is encapsulated.

</td>
</tr>
</table> 


## -remarks



This interface is used by a transform implementation to first describe and then indicate changes to the rendering pass that corresponds to the transform.




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

