---
UID: NN:d2d1_3.ID2D1InkStyle
title: ID2D1InkStyle
author: windows-sdk-content
description: Represents a collection of style properties to be used by methods like ID2D1DeviceContext2::DrawInkwhen rendering ink. The ink style defines the nib (pen tip) shape and transform.
old-location: direct2d\id2d1inkstyle.htm
tech.root: direct2d
ms.assetid: 03853FA5-1377-42FB-A4C2-50069DDF6E2D
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID2D1InkStyle, ID2D1InkStyle interface [Direct2D], ID2D1InkStyle interface [Direct2D],described, d2d1_3/ID2D1InkStyle, direct2d.id2d1inkstyle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1InkStyle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1InkStyle interface


## -description


Represents a collection of style properties to be used by methods like <a href="https://msdn.microsoft.com/d7c27267-c0c3-d21c-7980-3d92396509c7">ID2D1DeviceContext2::DrawInk</a>when rendering ink. The ink style defines the nib (pen tip) shape and transform.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1InkStyle</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1InkStyle</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1InkStyle</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81A1AA30-9817-422C-A3AD-0BB3F2A02604">GetNibShape</a>
</td>
<td align="left" width="63%">
Retrieves the pre-transform nib shape for this style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A5ABCA78-BBA3-48EE-8A5E-BACDD2CDED37">GetNibTransform</a>
</td>
<td align="left" width="63%">
Retrieves the transform to be applied to this style's nib shape.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/460A037D-5315-4CAE-AB6B-5286B48551F1">SetNibShape</a>
</td>
<td align="left" width="63%">
Sets the pre-transform nib shape for this style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2caee05-192c-1ea5-103c-e1d44e8c30a8">SetNibTransform</a>
</td>
<td align="left" width="63%">Overloaded. Sets the transform to apply to this style's nib shape.

</td>
</tr>
</table> 

