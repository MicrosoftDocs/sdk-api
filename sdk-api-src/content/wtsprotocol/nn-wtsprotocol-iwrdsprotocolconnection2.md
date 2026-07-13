---
UID: NN:wtsprotocol.IWRdsProtocolConnection2
tech.root: TermServ
title: IWRdsProtocolConnection2
ms.date: 09/25/2025
targetos: Windows
description: 
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: wtsprotocol.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows, version 26100
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wtsprotocol.dll
api_name:
 - IWRdsProtocolConnection2
f1_keywords:
 - IWRdsProtocolConnection2
 - wtsprotocol/IWRdsProtocolConnection2
dev_langs:
 - c++
helpviewer_keywords:
 - IWRdsProtocolConnection2
---

## -description

Extends *[IWRdsProtocolConnection](/windows/win32/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)* to allow a protocol to provide serialized credentials to the Remote Desktop Services service for interactive logon. This interface is implemented by protocols. The Remote Desktop Services service calls **QueryInterface** on the *[IWRdsProtocolConnection](/windows/win32/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)* interface pointer it received from the protocol when it called *[IWRdsProtocolListenerCallback::OnConnected](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected)* method.

## -remarks

## -see-also

