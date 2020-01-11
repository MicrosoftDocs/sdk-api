---
UID: NN:d3d11_4.ID3D11Multithread
title: ID3D11Multithread (d3d11_4.h)
description: Provides threading protection for critical sections of a multi-threaded application.
old-location: direct3d11\id3d11multithread.htm
tech.root: direct3d11
ms.assetid: 1A07694E-7D61-4A59-82E3-048F04C8D57A
ms.date: 12/05/2018
ms.keywords: ID3D11Multithread, ID3D11Multithread interface [Direct3D 11], ID3D11Multithread interface [Direct3D 11],described, d3d11_4/ID3D11Multithread, direct3d11.id3d11multithread
f1_keywords:
- d3d11_4/ID3D11Multithread
dev_langs:
- c++
req.header: d3d11_4.h
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
req.lib: D3d11_4.lib
req.dll: D3d11_4.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d11_4.dll
api_name:
- ID3D11Multithread
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11Multithread interface


## -description


Provides threading protection for critical sections of a multi-threaded application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Multithread</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11Multithread</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Multithread</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-enter">Enter</a>
</td>
<td align="left" width="63%">
Enter a device's critical section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-getmultithreadprotected">GetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Find out if multithread protection is turned on or not.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-leave">Leave</a>
</td>
<td align="left" width="63%">
Leave a device's critical section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-setmultithreadprotected">SetMultithreadProtected</a>
</td>
<td align="left" width="63%">
Turns multithread protection on or off.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from an immediate device context created with the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> (or later versions of this) interface 
          using <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a>.

Unlike D3D10, there is no multithreaded layer in D3D11. By default, multithread protection is turned off. Use <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-setmultithreadprotected">SetMultithreadProtected</a> to turn it on, then <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-enter">Enter</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11multithread-leave">Leave</a> to encapsulate graphics commands that  must be executed in a specific order.

By default in D3D11, applications can only use one thread with the immediate context at a time. But, applications can use this interface to change that restriction. The interface can turn on threading protection for the immediate context, which will increase the overhead of each immediate context call in order to share one context with multiple threads.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

