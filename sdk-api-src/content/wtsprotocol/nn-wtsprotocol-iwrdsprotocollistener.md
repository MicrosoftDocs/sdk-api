---
UID: NN:wtsprotocol.IWRdsProtocolListener
title: IWRdsProtocolListener (wtsprotocol.h)
author: windows-sdk-content
description: Exposes methods that request that the protocol start and stop listening for client connection requests.
old-location: termserv\iwrdsprotocollistener.htm
tech.root: TermServ
ms.assetid: 19d3176a-3f47-46c1-8bee-8e0f1d9b466e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolListener, IWRdsProtocolListener interface [Remote Desktop Services], IWRdsProtocolListener interface [Remote Desktop Services],described, termserv.iwrdsprotocollistener, wtsprotocol/IWRdsProtocolListener
ms.topic: interface
f1_keywords: ["wtsprotocol/IWRdsProtocolListener"]
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
 - IWRdsProtocolListener
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolListener interface


## -description


Exposes methods that request that the protocol start and stop listening for client connection requests. The interface is implemented by the protocol, and its methods are called by the Remote Desktop Services service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolListener</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolListener</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolListener</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-getsettings">GetSettings</a>
</td>
<td align="left" width="63%">
Gets the listener setting information for client connection requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten">StartListen</a>
</td>
<td align="left" width="63%">
Notifies the protocol to start listening for client connection requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten">StopListen</a>
</td>
<td align="left" width="63%">
Notifies the protocol to stop listening for client connection requests.

</td>
</tr>
</table> 


## -remarks



To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.



