---
UID: NN:wtsprotocol.IWRdsEnhancedFastReconnectArbitrator
tech.root: TermServ
title: IWRdsEnhancedFastReconnectArbitrator
ms.date: 10/06/2021
ms.topic: language-reference
targetos: Windows
description: Exposes a method called by the Remote Desktop Services service to obtain the session ID that is to be reconnected to in the enhanced fast reconnect sequence.
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: wtsprotocol.h
req.idl: Wtsprotocol.idl
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2022
req.target-type: Windows
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsEnhancedFastReconnectArbitrator
f1_keywords:
 - IWRdsEnhancedFastReconnectArbitrator
 - wtsprotocol/IWRdsEnhancedFastReconnectArbitrator
dev_langs:
 - c++
---

## -description

Exposes a method called by the Remote Desktop Services service to obtain the session ID that is to be reconnected to in the enhanced fast reconnect sequence.

## -inheritance

The <b>IWRdsEnhancedFastReconnectArbitrator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

## -methods

The <b>IWRdsEnhancedFastReconnectArbitrator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsenhancedfastreconnectarbitrator-getsessionforenhancedfastreconnect">GetSessionForEnhancedFastReconnect</a>
</td>
<td align="left" width="63%">
The protocol stack uses this method to return the session ID to be used for enhanced fast reconnect.
</td>
</tr>

## -remarks

## -see-also
