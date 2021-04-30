---
UID: NF:wtsprotocol.IWTSProtocolManager.NotifySessionOfServiceStart
title: IWTSProtocolManager::NotifySessionOfServiceStart (wtsprotocol.h)
description: IWTSProtocolManager::NotifySessionOfServiceStart is no longer available. Instead, use IWRdsProtocolManager::NotifySessionOfServiceStart.
helpviewer_keywords: ["IWTSProtocolManager interface [Remote Desktop Services]","NotifySessionOfServiceStart method","IWTSProtocolManager.NotifySessionOfServiceStart","IWTSProtocolManager::NotifySessionOfServiceStart","NotifySessionOfServiceStart","NotifySessionOfServiceStart method [Remote Desktop Services]","NotifySessionOfServiceStart method [Remote Desktop Services]","IWTSProtocolManager interface","termserv.iwtsprotocolmanager_notifysessionofservicestart","wtsprotocol/IWTSProtocolManager::NotifySessionOfServiceStart"]
old-location: termserv\iwtsprotocolmanager_notifysessionofservicestart.htm
tech.root: TermServ
ms.assetid: 8b9e7578-75e1-4447-8ff9-e391bf339fbe
ms.date: 12/05/2018
ms.keywords: IWTSProtocolManager interface [Remote Desktop Services],NotifySessionOfServiceStart method, IWTSProtocolManager.NotifySessionOfServiceStart, IWTSProtocolManager::NotifySessionOfServiceStart, NotifySessionOfServiceStart, NotifySessionOfServiceStart method [Remote Desktop Services], NotifySessionOfServiceStart method [Remote Desktop Services],IWTSProtocolManager interface, termserv.iwtsprotocolmanager_notifysessionofservicestart, wtsprotocol/IWTSProtocolManager::NotifySessionOfServiceStart
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
 - IWTSProtocolManager::NotifySessionOfServiceStart
 - wtsprotocol/IWTSProtocolManager::NotifySessionOfServiceStart
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
 - IWTSProtocolManager.NotifySessionOfServiceStart
---

# IWTSProtocolManager::NotifySessionOfServiceStart


## -description

<p class="CCE_Message">[<b>IWTSProtocolManager::NotifySessionOfServiceStart</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-notifysessionofservicestart">IWRdsProtocolManager::NotifySessionOfServiceStart</a>.]

Notifies the protocol provider that the Remote Desktop Services service has started for a given session.

## -parameters

### -param SessionId [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wts_session_id">WTS_SESSION_ID</a> structure that uniquely identifies the session.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolmanager">IWTSProtocolManager</a>