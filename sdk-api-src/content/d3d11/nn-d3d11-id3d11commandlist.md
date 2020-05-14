---
UID: NN:d3d11.ID3D11CommandList
title: ID3D11CommandList (d3d11.h)
description: The ID3D11CommandList interface encapsulates a list of graphics commands for play back.helpviewer_keywords: ["6f498894-85b1-fe5f-e486-d12c2cb7a180","ID3D11CommandList","ID3D11CommandList interface [Direct3D 11]","ID3D11CommandList interface [Direct3D 11]","described","d3d11/ID3D11CommandList","direct3d11.id3d11commandlist"]
old-location: direct3d11\id3d11commandlist.htm
tech.root: direct3d11
ms.assetid: 432f1d21-bf13-4569-9c8f-04f5d2845150
ms.date: 12/05/2018
ms.keywords: 6f498894-85b1-fe5f-e486-d12c2cb7a180, ID3D11CommandList, ID3D11CommandList interface [Direct3D 11], ID3D11CommandList interface [Direct3D 11],described, d3d11/ID3D11CommandList, direct3d11.id3d11commandlist
f1_keywords:
- d3d11/ID3D11CommandList
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
- ID3D11CommandList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11CommandList interface


## -description


The <b>ID3D11CommandList</b> interface encapsulates a list of graphics commands for play back.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11CommandList</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11CommandList</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11commandlist-getcontextflags">GetContextFlags</a>
</td>
<td align="left" width="63%">
Gets the initialization flags associated with the deferred context that created the command list.

</td>
</tr>
</table> 


## -remarks



There is no explicit creation method, simply declare an <b>ID3D11CommandList</b> interface, then call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-finishcommandlist">ID3D11DeviceContext::FinishCommandList</a> to record commands or <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-executecommandlist">ID3D11DeviceContext::ExecuteCommandList</a> to play back commands.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>
 

 

