---
UID: NF:wtsprotocol.IWRdsProtocolManager.NotifyServiceStateChange
title: IWRdsProtocolManager::NotifyServiceStateChange (wtsprotocol.h)
description: Notifies the protocol provider that the state of the Remote Desktop Services service is changing.
helpviewer_keywords: ["IWRdsProtocolManager interface [Remote Desktop Services]","NotifyServiceStateChange method","IWRdsProtocolManager.NotifyServiceStateChange","IWRdsProtocolManager::NotifyServiceStateChange","NotifyServiceStateChange","NotifyServiceStateChange method [Remote Desktop Services]","NotifyServiceStateChange method [Remote Desktop Services]","IWRdsProtocolManager interface","termserv.iwrdsprotocolmanager_notifyservicestatechange","wtsprotocol/IWRdsProtocolManager::NotifyServiceStateChange"]
old-location: termserv\iwrdsprotocolmanager_notifyservicestatechange.htm
tech.root: TermServ
ms.assetid: 32b2a05a-d5de-4f2f-bcaa-587cf22aa5c5
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],NotifyServiceStateChange method, IWRdsProtocolManager.NotifyServiceStateChange, IWRdsProtocolManager::NotifyServiceStateChange, NotifyServiceStateChange, NotifyServiceStateChange method [Remote Desktop Services], NotifyServiceStateChange method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_notifyservicestatechange, wtsprotocol/IWRdsProtocolManager::NotifyServiceStateChange
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
 - IWRdsProtocolManager::NotifyServiceStateChange
 - wtsprotocol/IWRdsProtocolManager::NotifyServiceStateChange
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
 - IWRdsProtocolManager.NotifyServiceStateChange
---

# IWRdsProtocolManager::NotifyServiceStateChange


## -description

Notifies the protocol provider that the state of the Remote Desktop Services service is changing.

## -parameters

### -param pTSServiceStateChange [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_service_state">WRDS_SERVICE_STATE</a> structure that specifies 
whether the service is starting, stopping, or changing its drain state.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a>