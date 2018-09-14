---
UID: NN:d2d1effectauthor.ID2D1BlendTransform
title: ID2D1BlendTransform
author: windows-sdk-content
description: Provides methods to allow a blend operation to be inserted into a transform graph.
old-location: direct2d\id2d1blendtransform.htm
tech.root: Direct2D
ms.assetid: 0DC46758-6005-4A33-9539-9C95CF8CFB6A
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ID2D1BlendTransform, ID2D1BlendTransform interface [Direct2D], ID2D1BlendTransform interface [Direct2D],described, d2d1effectauthor/ID2D1BlendTransform, direct2d.id2d1blendtransform
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
 - ID2D1BlendTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1BlendTransform interface


## -description


Provides methods to allow a blend operation to be inserted into a transform graph.

The image output of the blend transform is the same as rendering an image effect graph with these steps:
<ul>
<li>Copy the first input to the destination image.</li>
<li>Render the next input on top using the blend description.</li>
<li>Continue for each additional input.</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1BlendTransform</b> interface inherits from <a href="https://msdn.microsoft.com/5349EF29-767F-4C78-A6F9-B0C6F143E762">ID2D1ConcreteTransform</a>. <b>ID2D1BlendTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1BlendTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7608A055-FD44-406E-86C7-DF575718D936">GetDescription</a>
</td>
<td align="left" width="63%">
Gets the blend description of the corresponding blend transform object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37E52B64-D998-4D85-858D-04A7751D7E0A">SetDescription</a>
</td>
<td align="left" width="63%">
Changes the blend description of the corresponding blend transform object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5349EF29-767F-4C78-A6F9-B0C6F143E762">ID2D1ConcreteTransform</a>



<a href="https://msdn.microsoft.com/6CA29200-9834-4A5B-99E8-434CD6E9B243">ID2D1TransformGraph</a>



<a href="https://msdn.microsoft.com/2ACF65DA-A812-4983-B044-71103A9AA450">ID2D1TransformNode</a>
 

 

