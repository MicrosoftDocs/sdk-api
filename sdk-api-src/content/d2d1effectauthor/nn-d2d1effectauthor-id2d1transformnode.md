---
UID: NN:d2d1effectauthor.ID2D1TransformNode
title: ID2D1TransformNode (d2d1effectauthor.h)
description: Describes a node in a transform topology.
old-location: direct2d\id2d1transformnode.htm
tech.root: Direct2D
ms.assetid: 2ACF65DA-A812-4983-B044-71103A9AA450
ms.date: 12/05/2018
ms.keywords: ID2D1TransformNode, ID2D1TransformNode interface [Direct2D], ID2D1TransformNode interface [Direct2D],described, d2d1effectauthor/ID2D1TransformNode, direct2d.id2d1transformnode
ms.topic: interface
f1_keywords:
- d2d1effectauthor/ID2D1TransformNode
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
- ID2D1TransformNode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1TransformNode interface


## -description


Describes a node in a transform topology.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1TransformNode</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1TransformNode</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1TransformNode</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformnode-getinputcount">GetInputCount</a>
</td>
<td align="left" width="63%">
Gets the number of inputs to the transform node.

</td>
</tr>
</table> 


## -remarks



Transform nodes are type-less and only define the notion of an object that accepts a number of inputs and is an output. This interface limits a topology to single output nodes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform">ID2D1BlendTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform">ID2D1Transform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph">ID2D1TransformGraph</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

