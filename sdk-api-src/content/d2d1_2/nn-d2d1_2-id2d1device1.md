---
UID: NN:d2d1_2.ID2D1Device1
title: ID2D1Device1 (d2d1_2.h)
author: windows-sdk-content
description: Represents a resource domain whose objects and device contexts can be used together.
old-location: direct2d\id2d1device1.htm
tech.root: Direct2D
ms.assetid: D0CC0F2C-2BAA-4BD6-AE67-BF99458160F9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1Device1, ID2D1Device1 interface [Direct2D], ID2D1Device1 interface [Direct2D],described, d2d1_2/ID2D1Device1, direct2d.id2d1device1
ms.topic: interface
req.header: d2d1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - ID2D1Device1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device1 interface


## -description


Represents a resource domain whose objects and device contexts can be used together. This interface performs all the same functions as the existing <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> interface. It also enables control of the device's rendering priority.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Device1</b> interface inherits from <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>. <b>ID2D1Device1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Device1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/204D74F1-3110-45F8-B034-15E3011F9D1F">GetRenderingPriority</a>
</td>
<td align="left" width="63%">
Retrieves the current rendering priority of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/520B4D0D-8D54-4599-9BA3-A03DBF35BCFF">SetRenderingPriority</a>
</td>
<td align="left" width="63%">
Sets the priority of Direct2D rendering operations performed on any device context associated with the device.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a>



<a href="https://msdn.microsoft.com/1C7B5FE0-23DB-417F-8614-53848D61A054">ID2D1Factory2::CreateDevice</a>
 

 

