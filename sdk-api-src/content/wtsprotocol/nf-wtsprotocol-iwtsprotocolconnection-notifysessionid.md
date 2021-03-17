---
UID: NF:wtsprotocol.IWTSProtocolConnection.NotifySessionId
title: IWTSProtocolConnection::NotifySessionId (wtsprotocol.h)
description: IWTSProtocolConnection::NotifySessionId is no longer available. Instead, use IWRdsProtocolConnection::NotifySessionId.
helpviewer_keywords: ["IWTSProtocolConnection interface [Remote Desktop Services]","NotifySessionId method","IWTSProtocolConnection.NotifySessionId","IWTSProtocolConnection::NotifySessionId","NotifySessionId","NotifySessionId method [Remote Desktop Services]","NotifySessionId method [Remote Desktop Services]","IWTSProtocolConnection interface","termserv.iwtsprotocolconnection_notifysessionid","wtsprotocol/IWTSProtocolConnection::NotifySessionId"]
old-location: termserv\iwtsprotocolconnection_notifysessionid.htm
tech.root: TermServ
ms.assetid: 5a545f66-7143-419d-9e0c-a96070472ce5
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],NotifySessionId method, IWTSProtocolConnection.NotifySessionId, IWTSProtocolConnection::NotifySessionId, NotifySessionId, NotifySessionId method [Remote Desktop Services], NotifySessionId method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_notifysessionid, wtsprotocol/IWTSProtocolConnection::NotifySessionId
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWTSProtocolConnection::NotifySessionId
 - wtsprotocol/IWTSProtocolConnection::NotifySessionId
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
 - IWTSProtocolConnection.NotifySessionId
---

# IWTSProtocolConnection::NotifySessionId


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::NotifySessionId</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-notifysessionid">IWRdsProtocolConnection::NotifySessionId</a>.]

Sends the ID of  the new session to the protocol.

## -parameters

### -param SessionId [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_session_id">WTS_SESSION_ID</a> structure that contains a connection GUID and the associated session ID.

## -remarks

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>