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

# IServerSecurity interface


## -description


Used by a server to help authenticate the client and to manage impersonation of the client. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServerSecurity</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IServerSecurity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServerSecurity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20398b63-0fcb-40ab-93ed-f4c75760eb9e">ImpersonateClient</a>
</td>
<td align="left" width="63%">
Enables a server to impersonate a client for the duration of a call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f847348a-1785-4b4a-b43e-a5eea21847c4">IsImpersonating</a>
</td>
<td align="left" width="63%">
Indicates whether the server is currently impersonating the client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a6fd68c-8e71-45f8-8a8e-c8a5f4f36868">QueryBlanket</a>
</td>
<td align="left" width="63%">
Retrieves information about the client that invoked one of the server's methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21952f54-439e-446f-a206-4b35759b1090">RevertToSelf</a>
</td>
<td align="left" width="63%">
Restores the authentication information of a thread to what it was before impersonation began.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b82e32c0-840d-402e-90d5-ff678c51faf1">CoGetCallContext</a>



<a href="https://msdn.microsoft.com/146855a2-97ec-4e71-88dc-316eaa1a24a0">CoSwitchCallContext</a>



<a href="https://msdn.microsoft.com/c9f6d06c-da24-48ea-908a-2462c33f7ee3">Security in COM</a>
 

 

