---
UID: NN:d2d1_1.ID2D1Device
title: ID2D1Device
author: windows-sdk-content
description: Represents a resource domain whose objects and device contexts can be used together.
old-location: direct2d\id2d1device.htm
tech.root: direct2d
ms.assetid: 21f77c38-c115-4fdf-b294-570577a29201
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ID2D1Device, ID2D1Device interface [Direct2D], ID2D1Device interface [Direct2D],described, d2d1_1/ID2D1Device, direct2d.id2d1device
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_1.h
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
 - ID2D1Device
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device interface


## -description


Represents a resource domain whose objects and device contexts can be used together.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Device</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1Device</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Device</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/310817b7-0548-4846-9d36-98842c06a450">ClearResources</a>
</td>
<td align="left" width="63%">
Clears all of the rendering resources used by Direct2D. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d14255d4-ae59-42b4-ada9-bd7a3c5e8024">CreateDeviceContext</a>
</td>
<td align="left" width="63%">
Creates a new device context from a Direct2D device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8860AEE-807A-435E-9F44-B50545320EDA">CreatePrintControl</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/0E8D8218-0671-44A2-AD6E-13BB0B4EB66C">ID2D1PrintControl</a> object that converts <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> primitives stored in <a href="https://msdn.microsoft.com/30b89f53-d20b-4070-abcd-ef95813130d1">ID2D1CommandList</a> into a fixed page representation.  The print sub-system then consumes the primitives.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0EAF3618-61A8-4332-8B62-1F37335A47A8">GetMaximumTextureMemory</a>
</td>
<td align="left" width="63%">
Sets the maximum amount of texture memory Direct2D accumulates before it purges the image caches and cached texture allocations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8B714995-8837-4605-8CA3-7D7941D2C10D">SetMaximumTextureMemory</a>
</td>
<td align="left" width="63%">
Sets the maximum amount of texture memory Direct2D accumulates before it purges the image caches and cached texture allocations.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5ed3ec21-b609-41b6-9568-6ede460bc395">D2D1CreateDevice</a>



<a href="https://msdn.microsoft.com/d16569c1-e366-45fe-9079-ed9eb894547b">ID2D1Factory1::CreateDevice</a>



<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>
 

 

