---
UID: NN:sbtsv.ITsSbGlobalStore
title: ITsSbGlobalStore
author: windows-driver-content
description: Exposes methods that query for target computers, sessions, environments, and farms that have been added to the Remote Desktop Connection Broker (RD Connection Broker) store.
old-location: termserv\itssbglobalstore.htm
old-project: TermServ
ms.assetid: d25b6f73-ee5f-40e4-9c49-fd48dd3990d2
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITsSbGlobalStore, ITsSbGlobalStore interface [Remote Desktop Services], ITsSbGlobalStore interface [Remote Desktop Services],described, sbtsv/ITsSbGlobalStore, termserv.itssbglobalstore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbGlobalStore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbGlobalStore interface


## -description


Exposes methods that query for target computers, sessions, environments, and farms that have been added 
to the Remote Desktop Connection Broker (RD Connection Broker) store. Plug-ins can obtain an instance of the global store from the <a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a> 
object that they retrieve during initialization.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbGlobalStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbGlobalStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbGlobalStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fb29524-61e3-4d1a-be98-45f61b796e9e">EnumerateEnvironmentsByProvider</a>
</td>
<td align="left" width="63%">
Returns an array that contains the environments present on the specified provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51c59f35-667c-4723-aa7b-e8250bbdabe9">EnumerateFarms</a>
</td>
<td align="left" width="63%">
Enumerates all the farms that have been added by the specified resource 
plug-in. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16fe9154-913a-4b7f-8ab5-ea8654b7cc98">EnumerateSessions</a>
</td>
<td align="left" width="63%">
Returns an array that contains sessions on the specified provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/939d967f-6846-4ef2-9943-a171eac6cb21">EnumerateTargets</a>
</td>
<td align="left" width="63%">
Returns an array that contains the specified targets present in the global store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14b9ca43-735d-43d1-bda5-d84cc9a7761a">GetFarmProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property of a farm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d710842a-9bd5-4791-8f6e-bac2fe07c93f">QuerySessionBySessionId</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/d6f4c66a-79c3-4bc1-889d-ec5715e359ce">ITsSbSession</a> object associated with the given 
session ID. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e89ed692-66e5-49ed-b5d9-69eefeeae66f">QueryTarget</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a> object for the given parameters.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

