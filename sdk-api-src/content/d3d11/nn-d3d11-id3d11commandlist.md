---
UID: NN:d3d11.ID3D11CommandList
title: ID3D11CommandList
author: windows-sdk-content
description: The ID3D11CommandList interface encapsulates a list of graphics commands for play back.
old-location: direct3d11\id3d11commandlist.htm
tech.root: direct3d11
ms.assetid: 432f1d21-bf13-4569-9c8f-04f5d2845150
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 6f498894-85b1-fe5f-e486-d12c2cb7a180, ID3D11CommandList, ID3D11CommandList interface [Direct3D 11], ID3D11CommandList interface [Direct3D 11],described, d3d11/ID3D11CommandList, direct3d11.id3d11commandlist
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ID3D11CommandList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11CommandList interface


## -description


The <b>ID3D11CommandList</b> interface encapsulates a list of graphics commands for play back.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11CommandList</b> interface inherits from <a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>. <b>ID3D11CommandList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11CommandList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3d98f3f-6e66-408e-baee-661afb65c0a4">GetContextFlags</a>
</td>
<td align="left" width="63%">
Gets the initialization flags associated with the deferred context that created the command list.

</td>
</tr>
</table> 


## -remarks



There is no explicit creation method, simply declare an <b>ID3D11CommandList</b> interface, then call <a href="https://msdn.microsoft.com/31e9d8b6-4173-4999-8772-75134d60d269">ID3D11DeviceContext::FinishCommandList</a> to record commands or <a href="https://msdn.microsoft.com/54e74f7d-b8a4-458d-bb39-3d8a824f06ef">ID3D11DeviceContext::ExecuteCommandList</a> to play back commands.




## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/bed17239-0358-4768-8655-9a1d92f25a2e">ID3D11DeviceChild</a>
 

 

