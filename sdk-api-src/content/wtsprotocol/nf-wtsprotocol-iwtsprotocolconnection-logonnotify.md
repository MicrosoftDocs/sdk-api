---
UID: NF:wtsprotocol.IWTSProtocolConnection.LogonNotify
title: IWTSProtocolConnection::LogonNotify (wtsprotocol.h)
description: IWTSProtocolConnection::LogonNotify is no longer available. Instead, use IWRdsProtocolConnection::LogonNotify.
helpviewer_keywords: ["IWTSProtocolConnection interface [Remote Desktop Services]","LogonNotify method","IWTSProtocolConnection.LogonNotify","IWTSProtocolConnection::LogonNotify","LogonNotify","LogonNotify method [Remote Desktop Services]","LogonNotify method [Remote Desktop Services]","IWTSProtocolConnection interface","termserv.iwtsprotocolconnection_logonnotify","wtsprotocol/IWTSProtocolConnection::LogonNotify"]
old-location: termserv\iwtsprotocolconnection_logonnotify.htm
tech.root: TermServ
ms.assetid: 6065e827-23a5-4150-bda5-999b7acede65
ms.date: 12/05/2018
ms.keywords: IWTSProtocolConnection interface [Remote Desktop Services],LogonNotify method, IWTSProtocolConnection.LogonNotify, IWTSProtocolConnection::LogonNotify, LogonNotify, LogonNotify method [Remote Desktop Services], LogonNotify method [Remote Desktop Services],IWTSProtocolConnection interface, termserv.iwtsprotocolconnection_logonnotify, wtsprotocol/IWTSProtocolConnection::LogonNotify
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
 - IWTSProtocolConnection::LogonNotify
 - wtsprotocol/IWTSProtocolConnection::LogonNotify
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
 - IWTSProtocolConnection.LogonNotify
---

# IWTSProtocolConnection::LogonNotify


## -description

<p class="CCE_Message">[<b>IWTSProtocolConnection::LogonNotify</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-logonnotify">IWRdsProtocolConnection::LogonNotify</a>.]

Specifies that the user has logged on to the session.

## -parameters

### -param hClientToken [in]

A pointer to a user token handle.

### -param wszUserName [in]

A pointer to a string that contains the user name.

### -param wszDomainName [in]

A pointer to a string that contains the domain name for the user.

### -param SessionId [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_session_id">WTS_SESSION_ID</a> structure that contains the session ID associated with the user.

## -remarks

The Remote Desktop Services service also calls this method when  the state of the session has changed.

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a <a href="/windows/desktop/TermServ/terminal-services-api-functions">Remote Desktop Services API</a> being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection">IWTSProtocolConnection</a>