---
UID: NF:wtsprotocol.IWTSProtocolConnection.AuthenticateClientToSession
title: IWTSProtocolConnection::AuthenticateClientToSession (wtsprotocol.h)
description: IWTSProtocolConnection::AuthenticateClientToSession is no longer available. Instead, use IWRdsProtocolConnection::AuthenticateClientToSession.
helpviewer_keywords: ["AuthenticateClientToSession","AuthenticateClientToSession method [Remote Desktop Services]","AuthenticateClientToSession method [Remote Desktop Services]","IWTSProtocolConnection interface","IWTSProtocolConnection interface [Remote Desktop Services]","AuthenticateClientToSession method","IWTSProtocolConnection.AuthenticateClientToSession","IWTSProtocolConnection::AuthenticateClientToSession","termserv.iwtsprotocolconnection_authenticateclienttosession","wtsprotocol/IWTSProtocolConnection::AuthenticateClientToSession"]
old-location: termserv\iwtsprotocolconnection_authenticateclienttosession.htm
tech.root: TermServ
ms.assetid: 541bf463-9a4a-4237-8a61-1288ab1540cc
ms.date: 12/05/2018
ms.keywords: AuthenticateClientToSession, AuthenticateClientToSession method [Remote Desktop Services], AuthenticateClientToSession method [Remote Desktop Services],IWTSProtocolConnection interface, IWTSProtocolConnection interface [Remote Desktop Services],AuthenticateClientToSession method, IWTSProtocolConnection.AuthenticateClientToSession, IWTSProtocolConnection::AuthenticateClientToSession, termserv.iwtsprotocolconnection_authenticateclienttosession, wtsprotocol/IWTSProtocolConnection::AuthenticateClientToSession
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
 - IWTSProtocolConnection::AuthenticateClientToSession
 - wtsprotocol/IWTSProtocolConnection::AuthenticateClientToSession
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
 - IWTSProtocolConnection.AuthenticateClientToSession
---

# IWTSProtocolConnection::AuthenticateClientToSession


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::AuthenticateClientToSession</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-authenticateclienttosession">IWRdsProtocolConnection::AuthenticateClientToSession</a>.]

Specifies a session that the connection should be reconnected to.

## -parameters

### -param SessionId [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_session_id">WTS_SESSION_ID</a> structure that uniquely identifies the session.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>