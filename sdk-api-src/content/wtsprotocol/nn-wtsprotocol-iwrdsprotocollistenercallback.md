---
UID: NN:wtsprotocol.IWRdsProtocolListenerCallback
title: IWRdsProtocolListenerCallback (wtsprotocol.h)
description: Exposes methods that notify the Remote Desktop Services service that a client has connected.helpviewer_keywords: ["IWRdsProtocolListenerCallback","IWRdsProtocolListenerCallback interface [Remote Desktop Services]","IWRdsProtocolListenerCallback interface [Remote Desktop Services]","described","termserv.iwrdsprotocollistenercallback","wtsprotocol/IWRdsProtocolListenerCallback"]
old-location: termserv\iwrdsprotocollistenercallback.htm
tech.root: TermServ
ms.assetid: 33f583a4-8311-4db1-9646-bed1cd06e479
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolListenerCallback, IWRdsProtocolListenerCallback interface [Remote Desktop Services], IWRdsProtocolListenerCallback interface [Remote Desktop Services],described, termserv.iwrdsprotocollistenercallback, wtsprotocol/IWRdsProtocolListenerCallback
f1_keywords:
- wtsprotocol/IWRdsProtocolListenerCallback
dev_langs:
- c++
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
- IWRdsProtocolListenerCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolListenerCallback interface


## -description


 Exposes methods that notify the Remote Desktop Services service that a client has connected. This interface is the callback object for the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener">IWRdsProtocolListener</a> interface. It is implemented by the Remote Desktop Services service and called by the protocol.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolListenerCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolListenerCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolListenerCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected">OnConnected</a>
</td>
<td align="left" width="63%">
Notifies the Remote Desktop Services service that a client connection request has been received.

</td>
</tr>
</table> 


## -remarks



To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.



