---
UID: NF:wtsprotocol.IWRdsProtocolConnection.PreDisconnect
title: IWRdsProtocolConnection::PreDisconnect (wtsprotocol.h)
description: Notifies the protocol that the session is about to be disconnected.
helpviewer_keywords: ["IWRdsProtocolConnection interface [Remote Desktop Services]","PreDisconnect method","IWRdsProtocolConnection.PreDisconnect","IWRdsProtocolConnection::PreDisconnect","PreDisconnect","PreDisconnect method [Remote Desktop Services]","PreDisconnect method [Remote Desktop Services]","IWRdsProtocolConnection interface","termserv.iwrdsprotocolconnection_predisconnect","wtsprotocol/IWRdsProtocolConnection::PreDisconnect"]
old-location: termserv\iwrdsprotocolconnection_predisconnect.htm
tech.root: TermServ
ms.assetid: 988032B5-94AA-40ED-B571-E7C2E652D023
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],PreDisconnect method, IWRdsProtocolConnection.PreDisconnect, IWRdsProtocolConnection::PreDisconnect, PreDisconnect, PreDisconnect method [Remote Desktop Services], PreDisconnect method [Remote Desktop Services],IWRdsProtocolConnection interface, termserv.iwrdsprotocolconnection_predisconnect, wtsprotocol/IWRdsProtocolConnection::PreDisconnect
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
 - IWRdsProtocolConnection::PreDisconnect
 - wtsprotocol/IWRdsProtocolConnection::PreDisconnect
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
 - IWRdsProtocolConnection.PreDisconnect
---

# IWRdsProtocolConnection::PreDisconnect


## -description

Notifies the protocol that the session is about to be disconnected.

## -parameters

### -param DisconnectReason [in]

A numeric value that indicates the reason for the disconnection.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>