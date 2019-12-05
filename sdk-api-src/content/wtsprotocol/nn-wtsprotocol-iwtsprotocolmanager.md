---
UID: NN:wtsprotocol.IWTSProtocolManager
title: IWTSProtocolManager (wtsprotocol.h)
description: IWTSProtocolManager is no longer available. Instead, use IWRdsProtocolManager.
old-location: termserv\iwtsprotocolmanager.htm
tech.root: TermServ
ms.assetid: a54bdb46-b18b-4a6d-90fc-75947f6dd191
ms.date: 12/05/2018
ms.keywords: IWTSProtocolManager, IWTSProtocolManager interface [Remote Desktop Services], IWTSProtocolManager interface [Remote Desktop Services],described, termserv.iwtsprotocolmanager, wtsprotocol/IWTSProtocolManager
ms.topic: interface
f1_keywords:
- wtsprotocol/IWTSProtocolManager
dev_langs:
- c++
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
- IWTSProtocolManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolManager interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolManager</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a>.]

Exposes methods that  the Remote Desktop Services service uses to communicate with the protocol provider. It is the only interface in the protocol provider for which the Remote Desktop Services service calls <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex">CoCreateInstanceEx</a>. In addition, the first call the Remote Desktop Services service makes into the protocol provider is to the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolmanager-createlistener">CreateListener</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolmanager-createlistener">CreateListener</a>
</td>
<td align="left" width="63%">
Requests the creation of an <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocollistener">IWTSProtocolListener</a> object that listens for incoming client connection requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolmanager-notifyservicestatechange">NotifyServiceStateChange</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider that the state of the Remote Desktop Services service is changing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolmanager-notifysessionofservicestart">NotifySessionOfServiceStart</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider that the Remote Desktop Services service has started for a given session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolmanager-notifysessionofservicestop">NotifySessionOfServiceStop</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider that the Remote Desktop Services service has stopped for a given session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolmanager-notifysessionstatechange">NotifySessionStateChange</a>
</td>
<td align="left" width="63%">
Notifies the protocol provider of changes in the state of a session. 

</td>
</tr>
</table> 

