---
UID: NF:wtsprotocol.IWRdsProtocolConnection.ConnectNotify
title: IWRdsProtocolConnection::ConnectNotify (wtsprotocol.h)
description: Signals the protocol that the session has been initialized.
helpviewer_keywords: ["ConnectNotify","ConnectNotify method [Remote Desktop Services]","ConnectNotify method [Remote Desktop Services]","IWRdsProtocolConnection interface","IWRdsProtocolConnection interface [Remote Desktop Services]","ConnectNotify method","IWRdsProtocolConnection.ConnectNotify","IWRdsProtocolConnection::ConnectNotify","termserv.iwrdsprotocolconnection_connectnotify","wtsprotocol/IWRdsProtocolConnection::ConnectNotify"]
old-location: termserv\iwrdsprotocolconnection_connectnotify.htm
tech.root: TermServ
ms.assetid: 057a093b-9b2d-4a2e-9593-fe0251427be0
ms.date: 12/05/2018
ms.keywords: ConnectNotify, ConnectNotify method [Remote Desktop Services], ConnectNotify method [Remote Desktop Services],IWRdsProtocolConnection interface, IWRdsProtocolConnection interface [Remote Desktop Services],ConnectNotify method, IWRdsProtocolConnection.ConnectNotify, IWRdsProtocolConnection::ConnectNotify, termserv.iwrdsprotocolconnection_connectnotify, wtsprotocol/IWRdsProtocolConnection::ConnectNotify
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
 - IWRdsProtocolConnection::ConnectNotify
 - wtsprotocol/IWRdsProtocolConnection::ConnectNotify
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
 - IWRdsProtocolConnection.ConnectNotify
---

# IWRdsProtocolConnection::ConnectNotify


## -description

Signals the protocol that the session has been initialized.

## -parameters

### -param SessionId [in]

The session identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>