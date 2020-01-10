---
UID: NN:wtsprotocol.IWTSProtocolShadowCallback
title: IWTSProtocolShadowCallback (wtsprotocol.h)
description: IWTSProtocolShadowCallback is no longer available. Instead, use IWRdsProtocolShadowCallback.
old-location: termserv\iwtsprotocolshadowcallback.htm
tech.root: TermServ
ms.assetid: ce224b9f-161c-4133-97d9-05c339eefb77
ms.date: 12/05/2018
ms.keywords: IWTSProtocolShadowCallback, IWTSProtocolShadowCallback interface [Remote Desktop Services], IWTSProtocolShadowCallback interface [Remote Desktop Services],described, termserv.iwtsprotocolshadowcallback, wtsprotocol/IWTSProtocolShadowCallback
f1_keywords:
- wtsprotocol/IWTSProtocolShadowCallback
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
- IWTSProtocolShadowCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWTSProtocolShadowCallback interface


## -description


<p class="CCE_Message">[<b>IWTSProtocolShadowCallback</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback">IWRdsProtocolShadowCallback</a>.]

 Exposes methods called by the protocol to notify the Remote Desktop Services service to start or stop the target side of a shadow. This interface is the callback interface for the <a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolshadowconnection">IWTSProtocolShadowConnection</a> interface. It is implemented by the Remote Desktop Services service and called by the protocol provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSProtocolShadowCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSProtocolShadowCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSProtocolShadowCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolshadowcallback-invoketargetshadow">InvokeTargetShadow</a>
</td>
<td align="left" width="63%">
Instructs the Remote Desktop Services service to begin the target side of the shadow and passes any information that must be exchanged between the client and the target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwtsprotocolshadowcallback-stopshadow">StopShadow</a>
</td>
<td align="left" width="63%">
Instructs the Remote Desktop Services service to stop shadowing a target.

</td>
</tr>
</table> 

