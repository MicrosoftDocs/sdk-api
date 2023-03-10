---
UID: NF:wtsprotocol.IWTSProtocolManager.NotifyServiceStateChange
title: IWTSProtocolManager::NotifyServiceStateChange (wtsprotocol.h)
description: IWTSProtocolManager::NotifyServiceStateChange is no longer available. Instead, use IWRdsProtocolManager::NotifyServiceStateChange.
helpviewer_keywords: ["IWTSProtocolManager interface [Remote Desktop Services]","NotifyServiceStateChange method","IWTSProtocolManager.NotifyServiceStateChange","IWTSProtocolManager::NotifyServiceStateChange","NotifyServiceStateChange","NotifyServiceStateChange method [Remote Desktop Services]","NotifyServiceStateChange method [Remote Desktop Services]","IWTSProtocolManager interface","termserv.iwtsprotocolmanager_notifyservicestatechange","wtsprotocol/IWTSProtocolManager::NotifyServiceStateChange"]
old-location: termserv\iwtsprotocolmanager_notifyservicestatechange.htm
tech.root: TermServ
ms.assetid: 303a53b3-b297-486c-9422-706ec60441f2
ms.date: 12/05/2018
ms.keywords: IWTSProtocolManager interface [Remote Desktop Services],NotifyServiceStateChange method, IWTSProtocolManager.NotifyServiceStateChange, IWTSProtocolManager::NotifyServiceStateChange, NotifyServiceStateChange, NotifyServiceStateChange method [Remote Desktop Services], NotifyServiceStateChange method [Remote Desktop Services],IWTSProtocolManager interface, termserv.iwtsprotocolmanager_notifyservicestatechange, wtsprotocol/IWTSProtocolManager::NotifyServiceStateChange
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
 - IWTSProtocolManager::NotifyServiceStateChange
 - wtsprotocol/IWTSProtocolManager::NotifyServiceStateChange
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
 - IWTSProtocolManager.NotifyServiceStateChange
---

# IWTSProtocolManager::NotifyServiceStateChange


## -description

<p class="CCE_Message">[<b>IWTSProtocolManager::NotifyServiceStateChange</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-notifyservicestatechange">IWRdsProtocolManager::NotifyServiceStateChange</a>.]

Notifies the protocol provider that the state of the Remote Desktop Services service is changing.

## -parameters

### -param pTSServiceStateChange [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_service_state">WTS_SERVICE_STATE</a> structure that specifies 
whether the service is starting, stopping, or changing its drain state.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager">IWTSProtocolManager</a>