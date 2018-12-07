---
UID: NN:d2d1effectauthor.ID2D1TransformNode
title: ID2D1TransformNode
author: windows-sdk-content
description: Describes a node in a transform topology.
old-location: direct2d\id2d1transformnode.htm
tech.root: direct2d
ms.assetid: 2ACF65DA-A812-4983-B044-71103A9AA450
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1TransformNode, ID2D1TransformNode interface [Direct2D], ID2D1TransformNode interface [Direct2D],described, d2d1effectauthor/ID2D1TransformNode, direct2d.id2d1transformnode
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID2D1TransformNode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1TransformNode interface


## -description


Describes a node in a transform topology.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1TransformNode</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1TransformNode</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8F8D2BD1-AF03-4EEA-8F5E-DED174074333">GetInputCount</a>
</td>
<td align="left" width="63%">
Gets the number of inputs to the transform node.

</td>
</tr>
</table> 


## -remarks



Transform nodes are type-less and only define the notion of an object that accepts a number of inputs and is an output. This interface limits a topology to single output nodes.




## -see-also




<a href="https://msdn.microsoft.com/0DC46758-6005-4A33-9539-9C95CF8CFB6A">ID2D1BlendTransform</a>



<a href="https://msdn.microsoft.com/8A0CD795-A6D8-4817-9676-58C11DDAAEBD">ID2D1Transform</a>



<a href="https://msdn.microsoft.com/6CA29200-9834-4A5B-99E8-434CD6E9B243">ID2D1TransformGraph</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

