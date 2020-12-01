---
UID: NF:wtsprotocol.IWRdsProtocolManager.NotifySessionStateChange
title: IWRdsProtocolManager::NotifySessionStateChange (wtsprotocol.h)
description: Notifies the protocol provider of changes in the state of a session.
helpviewer_keywords: ["IWRdsProtocolManager interface [Remote Desktop Services]","NotifySessionStateChange method","IWRdsProtocolManager.NotifySessionStateChange","IWRdsProtocolManager::NotifySessionStateChange","NotifySessionStateChange","NotifySessionStateChange method [Remote Desktop Services]","NotifySessionStateChange method [Remote Desktop Services]","IWRdsProtocolManager interface","WTS_CONSOLE_CONNECT","WTS_CONSOLE_DISCONNECT","WTS_REMOTE_CONNECT","WTS_SESSION_LOCK","WTS_SESSION_LOGOFF","WTS_SESSION_REMOTE_CONTROL","WTS_SESSION_UNLOCK","termserv.iwrdsprotocolmanager_notifysessionstatechange","wtsprotocol/IWRdsProtocolManager::NotifySessionStateChange"]
old-location: termserv\iwrdsprotocolmanager_notifysessionstatechange.htm
tech.root: TermServ
ms.assetid: 72438718-1a66-473b-a563-67cfc8095318
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],NotifySessionStateChange method, IWRdsProtocolManager.NotifySessionStateChange, IWRdsProtocolManager::NotifySessionStateChange, NotifySessionStateChange, NotifySessionStateChange method [Remote Desktop Services], NotifySessionStateChange method [Remote Desktop Services],IWRdsProtocolManager interface, WTS_CONSOLE_CONNECT, WTS_CONSOLE_DISCONNECT, WTS_REMOTE_CONNECT, WTS_SESSION_LOCK, WTS_SESSION_LOGOFF, WTS_SESSION_REMOTE_CONTROL, WTS_SESSION_UNLOCK, termserv.iwrdsprotocolmanager_notifysessionstatechange, wtsprotocol/IWRdsProtocolManager::NotifySessionStateChange
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
 - IWRdsProtocolManager::NotifySessionStateChange
 - wtsprotocol/IWRdsProtocolManager::NotifySessionStateChange
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
 - IWRdsProtocolManager.NotifySessionStateChange
---

# IWRdsProtocolManager::NotifySessionStateChange


## -description

Notifies the protocol provider of changes in the state of a session.

## -parameters

### -param SessionId [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_session_id">WRDS_SESSION_ID</a> structure that uniquely identifies the session.

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

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a>