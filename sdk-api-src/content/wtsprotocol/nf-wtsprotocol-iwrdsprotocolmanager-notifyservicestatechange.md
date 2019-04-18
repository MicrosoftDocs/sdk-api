---
UID: NF:wtsprotocol.IWRdsProtocolManager.NotifyServiceStateChange
title: IWRdsProtocolManager::NotifyServiceStateChange (wtsprotocol.h)
author: windows-sdk-content
description: Notifies the protocol provider that the state of the Remote Desktop Services service is changing.
old-location: termserv\iwrdsprotocolmanager_notifyservicestatechange.htm
tech.root: TermServ
ms.assetid: 32b2a05a-d5de-4f2f-bcaa-587cf22aa5c5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],NotifyServiceStateChange method, IWRdsProtocolManager.NotifyServiceStateChange, IWRdsProtocolManager::NotifyServiceStateChange, NotifyServiceStateChange, NotifyServiceStateChange method [Remote Desktop Services], NotifyServiceStateChange method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_notifyservicestatechange, wtsprotocol/IWRdsProtocolManager::NotifyServiceStateChange
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
 - IWRdsProtocolManager.NotifyServiceStateChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWRdsProtocolManager::NotifyServiceStateChange


## -description


Notifies the protocol provider that the state of the Remote Desktop Services service is changing.


## -parameters




### -param pTSServiceStateChange [in]

A pointer to a <a href="https://msdn.microsoft.com/5f4469f5-5a64-4292-bbe6-cc030f1421f5">WRDS_SERVICE_STATE</a> structure that specifies 
whether the service is starting, stopping, or changing its drain state.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a>
 

 

