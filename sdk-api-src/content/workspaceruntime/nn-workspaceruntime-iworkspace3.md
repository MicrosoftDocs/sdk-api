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

# IWorkspace3 interface


## -description


Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds 
   the ability to retrieve or set a claims token.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWorkspace3</b> interface inherits from <a href="https://msdn.microsoft.com/8155cd78-4c6b-47a9-a2c7-f9fffc95f700">IWorkspace2</a>. <b>IWorkspace3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWorkspace3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d615b999-0713-4d16-a89b-b5b208a76124">GetClaimsToken2</a>
</td>
<td align="left" width="63%">
Sets the claims token.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/221b0e8f-b43a-4942-9e70-152daf5b1ef0">SetClaimsToken</a>
</td>
<td align="left" width="63%">
Retrieves the claims token.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8155cd78-4c6b-47a9-a2c7-f9fffc95f700">IWorkspace2</a>



<a href="https://msdn.microsoft.com/4580df05-5e44-40d0-8765-5d9b4e1d339e">RemoteApp and Desktop Connection Runtime interfaces</a>
 

 

