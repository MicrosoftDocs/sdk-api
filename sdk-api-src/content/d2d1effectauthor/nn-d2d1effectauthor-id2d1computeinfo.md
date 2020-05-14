---
UID: NN:d2d1effectauthor.ID2D1ComputeInfo
title: ID2D1ComputeInfo (d2d1effectauthor.h)
description: Enables specification of information for a compute-shader rendering pass.helpviewer_keywords: ["ID2D1ComputeInfo","ID2D1ComputeInfo interface [Direct2D]","ID2D1ComputeInfo interface [Direct2D]","described","d2d1effectauthor/ID2D1ComputeInfo","direct2d.id2d1computeinfo"]
old-location: direct2d\id2d1computeinfo.htm
tech.root: Direct2D
ms.assetid: 0560BB4B-B837-4DA8-AD68-545224152BA5
ms.date: 12/05/2018
ms.keywords: ID2D1ComputeInfo, ID2D1ComputeInfo interface [Direct2D], ID2D1ComputeInfo interface [Direct2D],described, d2d1effectauthor/ID2D1ComputeInfo, direct2d.id2d1computeinfo
f1_keywords:
- d2d1effectauthor/ID2D1ComputeInfo
dev_langs:
- c++
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
- ID2D1ComputeInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1ComputeInfo interface


## -description


Enables specification of information for a compute-shader rendering pass.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1ComputeInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1ComputeInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1ComputeInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshader">SetComputeShader</a>
</td>
<td align="left" width="63%">
Sets the compute shader to the given shader resource.  The resource must be loaded before this call is made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer">SetComputeShaderConstantBuffer</a>
</td>
<td align="left" width="63%">
Establishes or changes the constant buffer data for this transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setresourcetexture">SetResourceTexture</a>
</td>
<td align="left" width="63%">
Sets the resource texture corresponding to the given shader texture index to the given texture resource.

</td>
</tr>
</table> 


## -remarks



The transform changes the state on this render information to specify the compute shader and its dependent resources.



