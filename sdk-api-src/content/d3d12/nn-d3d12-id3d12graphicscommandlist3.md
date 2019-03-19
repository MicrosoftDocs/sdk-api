---
UID: NN:d3d12.ID3D12GraphicsCommandList3
title: ID3D12GraphicsCommandList3 (d3d12.h)
author: windows-sdk-content
description: Encapsulates a list of graphics commands for rendering.
old-location: direct3d12\id3d12graphicscommandlist3.htm
tech.root: direct3d12
ms.assetid: 934CB757-495A-45DA-A942-1852D8E94934
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D12GraphicsCommandList3, ID3D12GraphicsCommandList3 interface, ID3D12GraphicsCommandList3 interface,described, d3d12/ID3D12GraphicsCommandList3, direct3d12.id3d12graphicscommandlist3
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList3 interface


## -description


Encapsulates a list of graphics commands for rendering.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList3</b> interface inherits from <a href="https://msdn.microsoft.com/6A1BF079-CAE7-45E9-A95F-E19ACD380143">ID3D12GraphicsCommandList2</a>. <b>ID3D12GraphicsCommandList3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12GraphicsCommandList3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5D176919-34DC-4FD5-A577-78B03D5AB76B">SetProtectedResourceSession</a>
</td>
<td align="left" width="63%">
Specifies whether or not protected resources can be accessed by subsequent commands in the command list. By default, no protected resources are enabled. After calling <a href="https://msdn.microsoft.com/5D176919-34DC-4FD5-A577-78B03D5AB76B">SetProtectedResourceSession</a> with a valid session, protected resources of the same type can refer to that session. After calling <b>SetProtectedResourceSession</b> with <b>NULL</b>, no protected resources can be accessed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6A1BF079-CAE7-45E9-A95F-E19ACD380143">ID3D12GraphicsCommandList2</a>
 

 

