---
UID: NF:wtsprotocol.IWTSProtocolConnection.ConnectNotify
title: IWTSProtocolConnection::ConnectNotify (wtsprotocol.h)
description: IWTSProtocolConnection::ConnectNotify is no longer available. Instead, use IWRdsProtocolConnection::ConnectNotify.
helpviewer_keywords: ["ConnectNotify","ConnectNotify method [Remote Desktop Services]","ConnectNotify method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","ConnectNotify method","IWTSProtocolConnection.ConnectNotify","IWTSProtocolConnection::ConnectNotify","termserv.iwtsprotocolconnection_connectnotify","wtsprotocol/IWTSProtocolConnection::ConnectNotify"]
old-location: termserv\iwtsprotocolconnection_connectnotify.htm
tech.root: TermServ
ms.assetid: 9109d867-d9dc-4b95-a674-9f59ed7aa6a4
ms.date: 12/05/2018
ms.keywords: ConnectNotify, ConnectNotify method [Remote Desktop Services], ConnectNotify method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],ConnectNotify method, IWTSProtocolConnection.ConnectNotify, IWTSProtocolConnection::ConnectNotify, termserv.iwtsprotocolconnection_connectnotify, wtsprotocol/IWTSProtocolConnection::ConnectNotify
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
 - IWTSProtocolConnection::ConnectNotify
 - wtsprotocol/IWTSProtocolConnection::ConnectNotify
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
 - IWTSProtocolConnection.ConnectNotify
---

# IWTSProtocolConnection::ConnectNotify


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::ConnectNotify</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-connectnotify">IWRdsProtocolConnection::ConnectNotify</a>.]

Signals that the session has been initialized.

## -parameters

### -param SessionId [in]

An integer that contains the session ID associated with the client.

## -remarks

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>