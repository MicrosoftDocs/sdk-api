---
UID: NN:d2d1_3.ID2D1Device2
title: ID2D1Device2
author: windows-sdk-content
description: Represents a resource domain whose objects and device contexts can be used together. This interface performs all the same functions as the existing ID2D1Device1 interface. It also enables the creation of ID2D1DeviceContext2 objects.
old-location: direct2d\id2d1device2.htm
tech.root: direct2d
ms.assetid: 1B34AEFD-BBA7-4759-B80A-89D9BFC1933D
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID2D1Device2, ID2D1Device2 interface [Direct2D], ID2D1Device2 interface [Direct2D],described, d2d1_3/ID2D1Device2, direct2d.id2d1device2
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
 - ID2D1Device2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Device2 interface


## -description


Represents a resource domain whose objects and device contexts can be used together.
          This interface performs all the same functions as the existing <a href="https://msdn.microsoft.com/D0CC0F2C-2BAA-4BD6-AE67-BF99458160F9">ID2D1Device1</a> interface.
          It also enables the creation of <a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a> objects.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Device2</b> interface inherits from <a href="https://msdn.microsoft.com/D0CC0F2C-2BAA-4BD6-AE67-BF99458160F9">ID2D1Device1</a>. <b>ID2D1Device2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Device2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92BC91A0-CD67-4F7B-9B8A-1301DD14C35C">CreateDeviceContext</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/25c11cfc-75af-20a1-8f54-6b370942b841">ID2D1DeviceContext2</a> from a Direct2D device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/914A64BA-61CD-4A66-91D8-F7CC040AF67A">FlushDeviceContexts</a>
</td>
<td align="left" width="63%">
Flush all device contexts that reference a given bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0495244-d641-24d8-f1e2-0de1e8f84426">GetDxgiDevice</a>
</td>
<td align="left" width="63%">
Returns the DXGI device associated with this Direct2D device.

</td>
</tr>
</table> 

