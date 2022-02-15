---
UID: NF:wtsprotocol.IWRdsProtocolConnection.LogonNotify
title: IWRdsProtocolConnection::LogonNotify (wtsprotocol.h)
description: Called when the user has logged on to the session.
helpviewer_keywords: ["IWRdsProtocolConnection interface [Remote Desktop Services]","LogonNotify method","IWRdsProtocolConnection.LogonNotify","IWRdsProtocolConnection::LogonNotify","LogonNotify","LogonNotify method [Remote Desktop Services]","LogonNotify method [Remote Desktop Services]","IWRdsProtocolConnection interface","termserv.iwrdsprotocolconnection_logonnotify","wtsprotocol/IWRdsProtocolConnection::LogonNotify"]
old-location: termserv\iwrdsprotocolconnection_logonnotify.htm
tech.root: TermServ
ms.assetid: 2b6ce1cd-0e9f-465d-a5d6-e0d35bddebc4
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolConnection interface [Remote Desktop Services],LogonNotify method, IWRdsProtocolConnection.LogonNotify, IWRdsProtocolConnection::LogonNotify, LogonNotify, LogonNotify method [Remote Desktop Services], LogonNotify method [Remote Desktop Services],IWRdsProtocolConnection interface, termserv.iwrdsprotocolconnection_logonnotify, wtsprotocol/IWRdsProtocolConnection::LogonNotify
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
 - IWRdsProtocolConnection::LogonNotify
 - wtsprotocol/IWRdsProtocolConnection::LogonNotify
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
 - IWRdsProtocolConnection.LogonNotify
---

# IWRdsProtocolConnection::LogonNotify


## -description

Called when the user has logged on to the session.

## -parameters

### -param hClientToken [in]

A handle that represents the user token.

### -param wszUserName [in]

A pointer to a null-terminated string that contains the user name.

### -param wszDomainName [in]

A pointer to a null-terminated string that contains the user's domain name.

### -param SessionId [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_session_id">WRDS_SESSION_ID</a> structure that uniquely identifies the session.

### -param pWRdsConnectionSettings [in, out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_connection_settings">WRDS_CONNECTION_SETTINGS</a> structure that contains connection settings for the session.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an event notification and you should return immediately from this method. To avoid a possible deadlock, you should not make any function or method calls that will directly or indirectly result in a Remote Desktop Services API being called. If you need to make any outbound call, you should start a new thread and make the outbound call from the new thread.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection">IWRdsProtocolConnection</a>