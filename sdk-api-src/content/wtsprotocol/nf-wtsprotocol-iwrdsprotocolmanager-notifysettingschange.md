---
UID: NF:wtsprotocol.IWRdsProtocolManager.NotifySettingsChange
title: IWRdsProtocolManager::NotifySettingsChange (wtsprotocol.h)
author: windows-sdk-content
description: Notifies the protocol provider of changes in the settings within the Remote Desktop Services service.
old-location: termserv\iwrdsprotocolmanager_notifysettingschange.htm
tech.root: TermServ
ms.assetid: 80292d9b-fced-4726-8f83-5ba355df06a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],NotifySettingsChange method, IWRdsProtocolManager.NotifySettingsChange, IWRdsProtocolManager::NotifySettingsChange, NotifySettingsChange, NotifySettingsChange method [Remote Desktop Services], NotifySettingsChange method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_notifysettingschange, wtsprotocol/IWRdsProtocolManager::NotifySettingsChange
ms.topic: method
f1_keywords:
- wtsprotocol/IWRdsProtocolManager.NotifySettingsChange
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wtsprotocol.h
api_name:
- IWRdsProtocolManager.NotifySettingsChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolManager::NotifySettingsChange


## -description


Notifies the protocol provider of changes in the settings within the Remote Desktop Services service.


## -parameters




### -param pWRdsSettings [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_settings">WRDS_SETTINGS</a> structure that contains the setting changes.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">IWRdsProtocolManager</a>
 

 

