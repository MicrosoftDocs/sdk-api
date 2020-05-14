---
UID: NN:d3d11.ID3D11Counter
title: ID3D11Counter (d3d11.h)
description: This interface encapsulates methods for measuring GPU performance.helpviewer_keywords: ["ID3D11Counter","ID3D11Counter interface [Direct3D 11]","ID3D11Counter interface [Direct3D 11]","described","d3d11/ID3D11Counter","direct3d11.id3d11counter","e8e19b70-2584-4e44-1faf-1bc2d275606a"]
old-location: direct3d11\id3d11counter.htm
tech.root: direct3d11
ms.assetid: 3f35b3d5-f829-443c-9ea6-6cffdd4f58b7
ms.date: 12/05/2018
ms.keywords: ID3D11Counter, ID3D11Counter interface [Direct3D 11], ID3D11Counter interface [Direct3D 11],described, d3d11/ID3D11Counter, direct3d11.id3d11counter, e8e19b70-2584-4e44-1faf-1bc2d275606a
f1_keywords:
- d3d11/ID3D11Counter
dev_langs:
- c++
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D11.lib
- D3D11.dll
api_name:
- ID3D11Counter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11Counter interface


## -description


This interface encapsulates methods for measuring GPU performance.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Counter</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>. <b>ID3D11Counter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Counter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11counter-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a counter description.

</td>
</tr>
</table> 


## -remarks



A counter can be created with <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createcounter">ID3D11Device::CreateCounter</a>.

This is a derived class of <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>.

Counter data is gathered by issuing an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> command, issuing some graphics commands, issuing an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a> command, and then calling <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> to get data about what happened in between the Begin and End calls. The data returned by GetData will be different depending on the type of counter. The call to End causes the data returned by GetData to be accurate up until the last call to End.

Counters are best suited for profiling.

For a list of the types of performance counters, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_counter">D3D11_COUNTER</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11asynchronous">ID3D11Asynchronous</a>
 

 

