---
UID: NN:d3d11_2.ID3D11Device2
title: ID3D11Device2 (d3d11_2.h)
author: windows-sdk-content
description: The device interface represents a virtual adapter; it is used to create resources. ID3D11Device2 adds new methods to those in ID3D11Device1.
old-location: direct3d11\id3d11device2.htm
tech.root: direct3d11
ms.assetid: C476AA0E-4A49-4E1E-8308-FB72EAD3E30C
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11Device2, ID3D11Device2 interface [Direct3D 11], ID3D11Device2 interface [Direct3D 11],described, d3d11_2/ID3D11Device2, direct3d11.id3d11device2
ms.topic: interface
f1_keywords: 
 - "d3d11_2/ID3D11Device2"
req.header: d3d11_2.h
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
 - ID3D11Device2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11Device2 interface


## -description


The device interface represents a virtual adapter; it is used to create resources. <b>ID3D11Device2</b> adds new methods to those in <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>. <b>ID3D11Device2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Device2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11device2-checkmultisamplequalitylevels1">CheckMultisampleQualityLevels1</a>
</td>
<td align="left" width="63%">
Get the number of quality levels available during multisampling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11device2-createdeferredcontext2">CreateDeferredContext2</a>
</td>
<td align="left" width="63%">
Creates a deferred context, which can record <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-command-list">command lists</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11device2-getimmediatecontext2">GetImmediateContext2</a>
</td>
<td align="left" width="63%">
Gets an immediate context, which can play back <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-command-list">command lists</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11device2-getresourcetiling">GetResourceTiling</a>
</td>
<td align="left" width="63%">
Gets info about how a tiled resource is broken into tiles.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1">ID3D11Device1</a>
 

 

