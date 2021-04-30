---
UID: NF:wtsprotocol.IWRdsProtocolManager.NotifySessionOfServiceStop
title: IWRdsProtocolManager::NotifySessionOfServiceStop (wtsprotocol.h)
description: Notifies the protocol provider that the Remote Desktop Services service has stopped for a given session.
helpviewer_keywords: ["IWRdsProtocolManager interface [Remote Desktop Services]","NotifySessionOfServiceStop method","IWRdsProtocolManager.NotifySessionOfServiceStop","IWRdsProtocolManager::NotifySessionOfServiceStop","NotifySessionOfServiceStop","NotifySessionOfServiceStop method [Remote Desktop Services]","NotifySessionOfServiceStop method [Remote Desktop Services]","IWRdsProtocolManager interface","termserv.iwrdsprotocolmanager_notifysessionofservicestop","wtsprotocol/IWRdsProtocolManager::NotifySessionOfServiceStop"]
old-location: termserv\iwrdsprotocolmanager_notifysessionofservicestop.htm
tech.root: TermServ
ms.assetid: acf52eb0-d8f8-4257-9c2c-e9345c0f1b7f
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],NotifySessionOfServiceStop method, IWRdsProtocolManager.NotifySessionOfServiceStop, IWRdsProtocolManager::NotifySessionOfServiceStop, NotifySessionOfServiceStop, NotifySessionOfServiceStop method [Remote Desktop Services], NotifySessionOfServiceStop method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_notifysessionofservicestop, wtsprotocol/IWRdsProtocolManager::NotifySessionOfServiceStop
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
 - IWRdsProtocolManager::NotifySessionOfServiceStop
 - wtsprotocol/IWRdsProtocolManager::NotifySessionOfServiceStop
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
 - IWRdsProtocolManager.NotifySessionOfServiceStop
---

# IWRdsProtocolManager::NotifySessionOfServiceStop


## -description

Notifies the protocol provider that the Remote Desktop Services service has stopped for a given session.

## -parameters

### -param SessionId [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_session_id">WRDS_SESSION_ID</a> structure that uniquely identifies the session.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a>