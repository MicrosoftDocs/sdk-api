---
UID: NN:wtsprotocol.IWRdsProtocolSettings
title: IWRdsProtocolSettings (wtsprotocol.h)
description: Exposes methods for retrieving and adding policy-related settings.
old-location: termserv\iwrdsprotocolsettings.htm
tech.root: TermServ
ms.assetid: 3680a001-e162-4930-985f-5c50c2e8a8b9
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolSettings, IWRdsProtocolSettings interface [Remote Desktop Services], IWRdsProtocolSettings interface [Remote Desktop Services],described, termserv.iwrdsprotocolsettings, wtsprotocol/IWRdsProtocolSettings
ms.topic: interface
f1_keywords:
- wtsprotocol/IWRdsProtocolSettings
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
- IWRdsProtocolSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolSettings interface


## -description


Exposes methods for retrieving and adding policy-related settings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsProtocolSettings</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWRdsProtocolSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWRdsProtocolSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolsettings-getsettings">GetSettings</a>
</td>
<td align="left" width="63%">
Retrieves the settings for a particular policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolsettings-mergesettings">MergeSettings</a>
</td>
<td align="left" width="63%">
Adds (merges) the specified policy-related settings into the larger group of connection settings.

</td>
</tr>
</table> 


## -remarks



To avoid a possible deadlock when calling any of the methods on this interface, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.



