---
UID: NF:wtsprotocol.IWTSProtocolManager.NotifySessionStateChange
title: IWTSProtocolManager::NotifySessionStateChange (wtsprotocol.h)
description: IWTSProtocolManager::NotifySessionStateChange is no longer available. Instead, use IWRdsProtocolManager::NotifySessionStateChange.
helpviewer_keywords: ["IWTSProtocolManager interface [Remote Desktop Services]","NotifySessionStateChange method","IWTSProtocolManager.NotifySessionStateChange","IWTSProtocolManager::NotifySessionStateChange","NotifySessionStateChange","NotifySessionStateChange method [Remote Desktop Services]","NotifySessionStateChange method [Remote Desktop Services]","IWTSProtocolManager interface","WTS_CONSOLE_CONNECT","WTS_CONSOLE_DISCONNECT","WTS_REMOTE_CONNECT","WTS_SESSION_LOCK","WTS_SESSION_LOGOFF","WTS_SESSION_REMOTE_CONTROL","WTS_SESSION_UNLOCK","termserv.iwtsprotocolmanager_notifysessionstatechange","wtsprotocol/IWTSProtocolManager::NotifySessionStateChange"]
old-location: termserv\iwtsprotocolmanager_notifysessionstatechange.htm
tech.root: TermServ
ms.assetid: 59c284bf-8175-46d2-ab44-8b2975574c14
ms.date: 12/05/2018
ms.keywords: IWTSProtocolManager interface [Remote Desktop Services],NotifySessionStateChange method, IWTSProtocolManager.NotifySessionStateChange, IWTSProtocolManager::NotifySessionStateChange, NotifySessionStateChange, NotifySessionStateChange method [Remote Desktop Services], NotifySessionStateChange method [Remote Desktop Services],IWTSProtocolManager interface, WTS_CONSOLE_CONNECT, WTS_CONSOLE_DISCONNECT, WTS_REMOTE_CONNECT, WTS_SESSION_LOCK, WTS_SESSION_LOGOFF, WTS_SESSION_REMOTE_CONTROL, WTS_SESSION_UNLOCK, termserv.iwtsprotocolmanager_notifysessionstatechange, wtsprotocol/IWTSProtocolManager::NotifySessionStateChange
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
 - IWTSProtocolManager::NotifySessionStateChange
 - wtsprotocol/IWTSProtocolManager::NotifySessionStateChange
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
 - IWTSProtocolManager.NotifySessionStateChange
---

# IWTSProtocolManager::NotifySessionStateChange


## -description

<p class="CCE_Message">[<b>IWTSProtocolManager::NotifySessionStateChange</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-notifysessionstatechange">IWRdsProtocolManager::NotifySessionStateChange</a>.]

Notifies the protocol provider of changes in the state of a session.

## -parameters

### -param SessionId [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_session_id">WTS_SESSION_ID</a> structure that uniquely identifies the session.

### -param EventId [in]

An integer that contains the event ID. The following IDs can be found in Winuser.h.



#### WTS_CONSOLE_CONNECT (0x1)



#### WTS_CONSOLE_DISCONNECT (0x2)



#### WTS_REMOTE_CONNECT (0x3)



#### WTS_SESSION_LOGOFF (0x6)



#### WTS_SESSION_LOCK (0x7)



#### WTS_SESSION_UNLOCK (0x8)



#### WTS_SESSION_REMOTE_CONTROL (0x9)

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager">IWTSProtocolManager</a>