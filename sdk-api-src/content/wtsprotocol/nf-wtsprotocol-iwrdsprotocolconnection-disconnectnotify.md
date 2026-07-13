---
UID: NF:wtsprotocol.IWRdsProtocolConnection.DisconnectNotify
title: IWRdsProtocolConnection::DisconnectNotify (wtsprotocol.h)
description: Notifies the protocol that the session has been disconnected.
helpviewer_keywords: ["DisconnectNotify","DisconnectNotify method [Remote Desktop Services]","DisconnectNotify method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","DisconnectNotify method","IWRdsProtocolConnection.DisconnectNotify","IWRdsProtocolConnection::DisconnectNotify","termserv.iwrdsprotocolconnection_disconnectnotify","wtsprotocol/IWRdsProtocolConnection::DisconnectNotify"]
old-location: termserv\iwrdsprotocolconnection_disconnectnotify.htm
tech.root: TermServ
ms.assetid: 2399677b-0859-4e43-9dbc-0b08fa0647b0
ms.date: 12/05/2018
ms.keywords: DisconnectNotify, DisconnectNotify method [Remote Desktop Services], DisconnectNotify method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],DisconnectNotify method, IWRdsProtocolConnection.DisconnectNotify, IWRdsProtocolConnection::DisconnectNotify, termserv.iwrdsprotocolconnection_disconnectnotify, wtsprotocol/IWRdsProtocolConnection::DisconnectNotify
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWRdsProtocolConnection::DisconnectNotify
 - wtsprotocol/IWRdsProtocolConnection::DisconnectNotify
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
 - IWRdsProtocolConnection.DisconnectNotify
---

# IWRdsProtocolConnection::DisconnectNotify


## -description

Notifies the protocol that the session has been disconnected.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>
