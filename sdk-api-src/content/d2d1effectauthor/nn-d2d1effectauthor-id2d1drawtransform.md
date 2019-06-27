---
UID: NN:d2d1effectauthor.ID2D1DrawTransform
title: ID2D1DrawTransform (d2d1effectauthor.h)
author: windows-sdk-content
description: A specialized implementation of the Shantzis calculations to a transform implemented on the GPU.
old-location: direct2d\id2d1drawtransform.htm
tech.root: Direct2D
ms.assetid: 90C49A9A-9297-44E6-9AB8-01C6847CA3F8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1DrawTransform, ID2D1DrawTransform interface [Direct2D], ID2D1DrawTransform interface [Direct2D],described, d2d1effectauthor/ID2D1DrawTransform, direct2d.id2d1drawtransform
ms.topic: interface
f1_keywords: 
 - "d2d1effectauthor/ID2D1DrawTransform"
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
 - ID2D1DrawTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1DrawTransform interface


## -description


A specialized implementation of the Shantzis calculations to a transform implemented on the GPU. These  calculations are described in the paper <a href="https://dl.acm.org/citation.cfm?id=192191">A model for efficient and flexible image computing</a>.

The information required to specify a “Pass” in the rendering algorithm on a Pixel Shader is passed to the implementation through the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo">SetDrawInfo</a> method. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1DrawTransform</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1DrawTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1DrawTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo">SetDrawInfo</a>
</td>
<td align="left" width="63%">
    Provides the GPU render info interface to the transform implementation.

</td>
</tr>
</table> 

