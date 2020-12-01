---
UID: NN:wtsprotocol.IWRdsEnhancedFastReconnectArbitrator
title: IWRdsEnhancedFastReconnectArbitrator (wtsprotocol.h)
description: Exposes a method called by the Remote Desktop Services service to obtain the session ID that is to be reconnected to in the Enhanced Fast Reconnect sequence.
helpviewer_keywords: ["IWRdsEnhancedFastReconnectArbitrator","IWRdsEnhancedFastReconnectArbitrator interface [Remote Desktop Services]","IWRdsEnhancedFastReconnectArbitrator interface [Remote Desktop Services]","described","termserv.iwrdsenhancedfastreconnectarbitrator","wtsprotocol/IWRdsEnhancedFastReconnectArbitrator"]
old-location: termserv\iwrdsenhancedfastreconnectarbitrator.htm
tech.root: TermServ
ms.assetid: 7cfec729-f919-47bd-b392-1abd8d8254c2
ms.date: 10/27/2020
ms.keywords: IWRdsEnhancedFastReconnectArbitrator, IWRdsEnhancedFastReconnectArbitrator interface [Remote Desktop Services], IWRdsEnhancedFastReconnectArbitrator interface [Remote Desktop Services],described, termserv.iwrdsenhancedfastreconnectarbitrator, wtsprotocol/IWRdsEnhancedFastReconnectArbitrator
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
ms.custom: 21H1
f1_keywords:
 - IWRdsEnhancedFastReconnectArbitrator
 - wtsprotocol/IWRdsEnhancedFastReconnectArbitrator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWRdsEnhancedFastReconnectArbitrator
---

# IWRdsEnhancedFastReconnectArbitrator interface


## -description

Exposes a method called by the Remote Desktop Services service to obtain the session ID that is to be reconnected to in the Enhanced Fast Reconnect sequence.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWRdsEnhancedFastReconnectArbitrator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. 

## -members

The <b>IWRdsEnhancedFastReconnectArbitrator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsenhancedfastreconnectarbitrator-getsessionforenhancedfastreconnect">GetSessionForEnhancedFastReconnect</a>
</td>
<td align="left" width="63%">
Protocol stack uses this method to return Session ID to be used for Enhanced Fast Reconnect.
</td>
</tr>
</table>