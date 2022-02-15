---
UID: NF:wtsprotocol.IWRdsProtocolConnection.NotifySessionId
title: IWRdsProtocolConnection::NotifySessionId (wtsprotocol.h)
description: Sends the identifier of the new session to the protocol.
helpviewer_keywords: ["IWRdsProtocolConnection interface [Remote Desktop Services]","NotifySessionId method","IWRdsProtocolConnection.NotifySessionId","IWRdsProtocolConnection::NotifySessionId","NotifySessionId","NotifySessionId method [Remote Desktop Services]","NotifySessionId method [Remote Desktop Services]","IWRdsProtocolConnection interface","termserv.iwrdsprotocolconnection_notifysessionid","wtsprotocol/IWRdsProtocolConnection::NotifySessionId"]
old-location: termserv\iwrdsprotocolconnection_notifysessionid.htm
tech.root: TermServ
ms.assetid: 82bf892e-5e6f-4057-ac36-00e046080c93
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],NotifySessionId method, IWRdsProtocolConnection.NotifySessionId, IWRdsProtocolConnection::NotifySessionId, NotifySessionId, NotifySessionId method [Remote Desktop Services], NotifySessionId method [Remote Desktop Services],IWRdsProtocolConnection interface, termserv.iwrdsprotocolconnection_notifysessionid, wtsprotocol/IWRdsProtocolConnection::NotifySessionId
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
 - IWRdsProtocolConnection::NotifySessionId
 - wtsprotocol/IWRdsProtocolConnection::NotifySessionId
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
 - IWRdsProtocolConnection.NotifySessionId
---

# IWRdsProtocolConnection::NotifySessionId


## -description

Sends the identifier of the new session to the protocol.

## -parameters

### -param SessionId [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_session_id">WRDS_SESSION_ID</a> structure that uniquely identifies the session.

### -param SessionHandle [in]

The session handle.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>