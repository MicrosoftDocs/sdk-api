---
UID: NN:wtsprotocol.IWRdsProtocolConnectionCallback
title: IWRdsProtocolConnectionCallback
author: windows-sdk-content
description: Exposes methods that provide information about the status of a client connection and that perform actions for the client. This interface is implemented by the Remote Desktop Services service and called by the protocol.
old-location: termserv\iwrdsprotocolconnectioncallback.htm
tech.root: termserv
ms.assetid: 81a73688-f39e-4960-8587-602d56c11e7e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IWRdsProtocolConnectionCallback, IWRdsProtocolConnectionCallback interface [Remote Desktop Services], IWRdsProtocolConnectionCallback interface [Remote Desktop Services],described, termserv.iwrdsprotocolconnectioncallback, wtsprotocol/IWRdsProtocolConnectionCallback
ms.prod: windows
ms.technology: windows-sdk
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
 - IWRdsProtocolConnectionCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolConnectionCallback interface


## -description


Exposes methods that provide information about the status of a client connection and that perform actions for the client. This interface is implemented by the Remote Desktop Services service and called by the protocol.

An instance of this interface is associated with a specific instance of the <a href="https://msdn.microsoft.com/2b8a5b2f-5a54-4d60-8b5a-8a914728087c">IWRdsProtocolConnection</a> interface. When the following documentation refers to a connection, it is therefore referring to the specific connection for which the  <b>IWRdsProtocolConnection</b> object was created.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolConnectionCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWRdsProtocolConnectionCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolConnectionCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc317e10-e09c-423b-8016-eb1cf49eba43">BrokenConnection</a>
</td>
<td align="left" width="63%">
Informs the Remote Desktop Services service that the client connection has been lost.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2EE03CA1-25D5-4B03-A2F1-EC167BD694B3">GetConnectionId</a>
</td>
<td align="left" width="63%">
Retrieves the connection identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88134a34-c494-48ea-9063-206e7d0c5139">OnReady</a>
</td>
<td align="left" width="63%">
Requests that the Remote Desktop Services service continue the connection process for that client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92d52015-c5b9-472e-898b-aca6f6e83620">RedrawWindow</a>
</td>
<td align="left" width="63%">
Requests that the Remote Desktop Services service redraw the client window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/698b59d3-8391-4101-801c-8d5fd701a757">StopScreenUpdates</a>
</td>
<td align="left" width="63%">
Requests that the Remote Desktop Services service stop updating the client screen.

</td>
</tr>
</table> 


## -remarks



To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.



