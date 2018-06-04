---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

