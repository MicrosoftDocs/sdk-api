---
UID: NN:wtsprotocol.IWRdsProtocolShadowCallback
title: IWRdsProtocolShadowCallback (wtsprotocol.h)
description: Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow.
helpviewer_keywords: ["IWRdsProtocolShadowCallback","IWRdsProtocolShadowCallback interface [Remote Desktop Services]","IWRdsProtocolShadowCallback interface [Remote Desktop Services]","described","termserv.iwrdsprotocolshadowcallback","wtsprotocol/IWRdsProtocolShadowCallback"]
old-location: termserv\iwrdsprotocolshadowcallback.htm
tech.root: TermServ
ms.assetid: 47727d33-df3d-49da-bc82-a4ed5ce0a381
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolShadowCallback, IWRdsProtocolShadowCallback interface [Remote Desktop Services], IWRdsProtocolShadowCallback interface [Remote Desktop Services],described, termserv.iwrdsprotocolshadowcallback, wtsprotocol/IWRdsProtocolShadowCallback
f1_keywords:
- wtsprotocol/IWRdsProtocolShadowCallback
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
- IWRdsProtocolShadowCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolShadowCallback interface


## -description


 Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow. This interface is the callback interface for the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection">IWRdsProtocolShadowConnection</a> interface. It is implemented by the Remote Desktop Services service and called by the protocol provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolShadowCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolShadowCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolShadowCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolshadowcallback-invoketargetshadow">InvokeTargetShadow</a>
</td>
<td align="left" width="63%">
Instructs the Remote Desktop Services service to begin the target side of the shadow and passes any information that must be exchanged between the client and the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolshadowcallback-stopshadow">StopShadow</a>
</td>
<td align="left" width="63%">
Instructs the Remote Desktop Services service to stop shadowing a target.

</td>
</tr>
</table> 

