---
UID: NN:wtsprotocol.IWTSProtocolLogonErrorRedirector
title: IWTSProtocolLogonErrorRedirector (wtsprotocol.h)
description: IWTSProtocolLogonErrorRedirector is no longer available. Instead, use IWRdsProtocolLogonErrorRedirector.
helpviewer_keywords: ["IWTSProtocolLogonErrorRedirector","IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services]","IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services]","described","termserv.iwtsprotocollogonerrorredirector","wtsprotocol/IWTSProtocolLogonErrorRedirector"]
old-location: termserv\iwtsprotocollogonerrorredirector.htm
tech.root: TermServ
ms.assetid: 1ff30217-9091-47df-a38f-30784538f0b9
ms.date: 12/05/2018
ms.keywords: IWTSProtocolLogonErrorRedirector, IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services], IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services],described, termserv.iwtsprotocollogonerrorredirector, wtsprotocol/IWTSProtocolLogonErrorRedirector
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolLogonErrorRedirector
 - wtsprotocol/IWTSProtocolLogonErrorRedirector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWTSProtocolLogonErrorRedirector
---

# IWTSProtocolLogonErrorRedirector interface


## -description

<p class="CCE_Message">[<b>IWTSProtocolLogonErrorRedirector</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector">IWRdsProtocolLogonErrorRedirector</a>.]

Exposes methods called by the Remote Desktop Services service to update logon status and determine how to direct logon error messages. This interface is implemented by the protocol.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolLogonErrorRedirector</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolLogonErrorRedirector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolLogonErrorRedirector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollogonerrorredirector-onbeginpainting">OnBeginPainting</a>
</td>
<td align="left" width="63%">
Notifies the protocol that the logon user interface is ready to begin painting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollogonerrorredirector-redirectlogonerror">RedirectLogonError</a>
</td>
<td align="left" width="63%">
Queries the protocol for the action to take in response to a logon error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollogonerrorredirector-redirectmessage">RedirectMessage</a>
</td>
<td align="left" width="63%">
Queries the protocol regarding how to redirect the logon message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocollogonerrorredirector-redirectstatus">RedirectStatus</a>
</td>
<td align="left" width="63%">
Queries the protocol regarding how to redirect the client logon status update.

</td>
</tr>
</table>