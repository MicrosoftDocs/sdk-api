---
UID: NN:wtsprotocol.IWRdsProtocolLogonErrorRedirector
title: IWRdsProtocolLogonErrorRedirector
author: windows-sdk-content
description: Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages.
old-location: termserv\iwrdsprotocollogonerrorredirector.htm
tech.root: TermServ
ms.assetid: 43c283f5-c902-49cc-81a0-15fc6316c7d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsProtocolLogonErrorRedirector, IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services], IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services],described, termserv.iwrdsprotocollogonerrorredirector, wtsprotocol/IWRdsProtocolLogonErrorRedirector
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolLogonErrorRedirector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolLogonErrorRedirector interface


## -description


Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages. This interface is implemented by the protocol.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolLogonErrorRedirector</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsProtocolLogonErrorRedirector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolLogonErrorRedirector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc044746-1127-44a3-993d-ca2445c99ff6">OnBeginPainting</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the logon user interface is ready to begin painting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86c919e9-2c45-45dd-8eee-7b50efb00cbb">RedirectLogonError</a>
</td>
<td align="left" width="63%">
Queries the protocol for the action to take in response to a logon error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b818e2b0-3d6c-4a56-8175-75b585553520">RedirectMessage</a>
</td>
<td align="left" width="63%">
Queries the protocol regarding how to redirect the logon message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1f6caec-6e26-4508-b19d-ac0e12758b28">RedirectStatus</a>
</td>
<td align="left" width="63%">
Queries the protocol regarding how to redirect the client logon status update.

</td>
</tr>
</table> 


## -remarks



To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.



