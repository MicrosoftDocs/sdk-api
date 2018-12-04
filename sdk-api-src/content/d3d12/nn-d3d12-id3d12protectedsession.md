---
UID: NN:d3d12.ID3D12ProtectedSession
title: ID3D12ProtectedSession
author: windows-sdk-content
description: Offers base functionality that allows for a consistent way to monitor the validity of a session across the different types of sessions.
old-location: direct3d12\id3d12protectedsession.htm
tech.root: direct3d12
ms.assetid: BBB87F18-A4F4-44E7-AFD8-803BD2C7C753
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: ID3D12ProtectedSession, ID3D12ProtectedSession interface, ID3D12ProtectedSession interface,described, d3d12/ID3D12ProtectedSession, direct3d12.id3d12protectedsession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# ID3D12ProtectedSession interface


## -description


Offers base functionality that allows for a consistent way to monitor the validity of a session across the different types of sessions.  The different types of sessions are <a href="direct3d12.id3d12protectedresourcesession">ID3D12ProtectedResourceSession</a>, <a href="direct3d12.id3d12cryptosession">ID3D12CryptoSession</a>, and <a href="direct3d12.id3d12cryptosessionpolicy">ID3D12CryptoSessionPolicy</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ProtectedSession</b> interface inherits from <a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a>. <b>ID3D12ProtectedSession</b> also has these types of members:
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
<a href="direct3d12.id3d12protectedsession_getsessionstatus">GetSessionStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the protected session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="direct3d12.id3d12protectedsession_getstatusfence">GetStatusFence</a>
</td>
<td align="left" width="63%">
Retrieves the fence for the protected session. From the fence, you can retrieve the current uniqueness validity value (using <a href="https://msdn.microsoft.com/2F2DDFC5-8D31-4BCE-B378-610C95D7805F">ID3D12Fence::GetCompletedValue</a>), and add monitors for changes to its value. This is a read-only fence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/AED60281-A6E4-4AAD-A106-6CA6E9BAEB9A">ID3D12DeviceChild</a>
 

 

