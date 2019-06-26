---
UID: NN:wtsprotocol.IWTSProtocolListenerCallback
title: IWTSProtocolListenerCallback (wtsprotocol.h)
author: windows-sdk-content
description: IWTSProtocolListenerCallback is no longer available. Instead, use IWRdsProtocolListenerCallback.
old-location: termserv\iwtsprotocollistenercallback.htm
tech.root: TermServ
ms.assetid: 607fcb85-4602-4651-b246-3e32c8868e47
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWTSProtocolListenerCallback, IWTSProtocolListenerCallback interface [Remote Desktop Services], IWTSProtocolListenerCallback interface [Remote Desktop Services],described, termserv.iwtsprotocollistenercallback, wtsprotocol/IWTSProtocolListenerCallback
ms.topic: interface
f1_keywords: 
 - "wtsprotocol/IWTSProtocolListenerCallback"
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IWTSProtocolListenerCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolListenerCallback interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolListenerCallback</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback">IWRdsProtocolListenerCallback</a>.]

 Exposes methods that notify the Remote Desktop Services service that a client has connected. This interface is the callback object for the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener">IWTSProtocolListener</a> interface. It is implemented by the Remote Desktop Services service and called by the protocol.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolListenerCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolListenerCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolListenerCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollistenercallback-onconnected">OnConnected</a>
</td>
<td align="left" width="63%">
Notifies the Remote Desktop Services service that a client connection request has been received.

</td>
</tr>
</table> 

