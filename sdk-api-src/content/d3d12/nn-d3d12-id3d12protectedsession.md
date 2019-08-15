---
UID: NN:d3d12.ID3D12ProtectedSession
title: ID3D12ProtectedSession (d3d12.h)
author: windows-sdk-content
description: Offers base functionality that allows for a consistent way to monitor the validity of a session across the different types of sessions.
old-location: direct3d12\id3d12protectedsession.htm
tech.root: direct3d12
ms.assetid: BBB87F18-A4F4-44E7-AFD8-803BD2C7C753
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12ProtectedSession, ID3D12ProtectedSession interface, ID3D12ProtectedSession interface,described, d3d12/ID3D12ProtectedSession, direct3d12.id3d12protectedsession
ms.topic: interface
f1_keywords: 
 - "d3d12/ID3D12ProtectedSession"
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12ProtectedSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12ProtectedSession interface

## -description

Offers base functionality that allows for a consistent way to monitor the validity of a session across the different types of sessions. The different types of sessions is of type [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession).

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ProtectedSession</b> interface inherits from <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild">ID3D12DeviceChild</a>. <b>ID3D12ProtectedSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12ProtectedSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/win32/api/d3d12/nf-d3d12-id3d12protectedsession-getsessionstatus">GetSessionStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the protected session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/en-us/windows/win32/api/mmc/nf-mmc-iconsole-settoolbar">GetStatusFence</a>
</td>
<td align="left" width="63%">
Retrieves the fence for the protected session. From the fence, you can retrieve the current uniqueness validity value (using <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue">ID3D12Fence::GetCompletedValue</a>), and add monitors for changes to its value. This is a read-only fence.

</td>
</tr>
</table> 

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild">ID3D12DeviceChild</a>