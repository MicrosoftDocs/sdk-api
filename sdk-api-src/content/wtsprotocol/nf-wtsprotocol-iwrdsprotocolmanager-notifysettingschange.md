---
UID: NF:wtsprotocol.IWRdsProtocolManager.NotifySettingsChange
title: IWRdsProtocolManager::NotifySettingsChange
author: windows-sdk-content
description: Notifies the protocol provider of changes in the settings within the Remote Desktop Services service.
old-location: termserv\iwrdsprotocolmanager_notifysettingschange.htm
tech.root: TermServ
ms.assetid: 80292d9b-fced-4726-8f83-5ba355df06a2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],NotifySettingsChange method, IWRdsProtocolManager.NotifySettingsChange, IWRdsProtocolManager::NotifySettingsChange, NotifySettingsChange, NotifySettingsChange method [Remote Desktop Services], NotifySettingsChange method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_notifysettingschange, wtsprotocol/IWRdsProtocolManager::NotifySettingsChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IWRdsProtocolManager::NotifySettingsChange


## -description


Notifies the protocol provider of changes in the settings within the Remote Desktop Services service.


## -parameters




### -param pWRdsSettings [in]

A pointer to a <a href="https://msdn.microsoft.com/38AD33F9-F955-4906-90E2-3FE5261A3E58">WRDS_SETTINGS</a> structure that contains the setting changes.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a>
 

 

