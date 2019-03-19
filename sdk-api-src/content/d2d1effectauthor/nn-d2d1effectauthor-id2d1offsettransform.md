---
UID: NN:d2d1effectauthor.ID2D1OffsetTransform
title: ID2D1OffsetTransform (d2d1effectauthor.h)
author: windows-sdk-content
description: Instructs the effect-rendering system to offset an input bitmap without inserting a rendering pass.
old-location: direct2d\id2d1offsettransform.htm
tech.root: Direct2D
ms.assetid: 0809C0FC-2F7B-49D8-A695-AD451C9BD17F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1OffsetTransform, ID2D1OffsetTransform interface [Direct2D], ID2D1OffsetTransform interface [Direct2D],described, d2d1effectauthor/ID2D1OffsetTransform, direct2d.id2d1offsettransform
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
 - ID2D1OffsetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1OffsetTransform interface


## -description


Instructs the effect-rendering system to offset an input bitmap without inserting a rendering pass.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1OffsetTransform</b> interface inherits from <a href="https://msdn.microsoft.com/2ACF65DA-A812-4983-B044-71103A9AA450">ID2D1TransformNode</a>. <b>ID2D1OffsetTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1OffsetTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC928758-4493-4D45-A52B-3E22A98BAF12">GetOffset</a>
</td>
<td align="left" width="63%">
Gets the offset currently in the offset transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4694BB45-4D26-4CB8-B0D3-560493D60D88">SetOffset</a>
</td>
<td align="left" width="63%">
Sets the offset in the current offset transform.

</td>
</tr>
</table> 


## -remarks



Because a rendering pass is not required, the interface derives from a transform node. This allows it to be inserted into a graph but does not allow an output buffer to be specified.




## -see-also




<a href="https://msdn.microsoft.com/A0A479F7-CB2C-4A9A-B482-2383A3A1A841">I2D1DeviceContext::CreateOffsetTransform</a>



<a href="https://msdn.microsoft.com/2ACF65DA-A812-4983-B044-71103A9AA450">ID2D1TransformNode</a>
 

 

