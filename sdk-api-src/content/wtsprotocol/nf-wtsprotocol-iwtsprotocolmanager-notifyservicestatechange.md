---
UID: NF:wtsprotocol.IWTSProtocolManager.NotifyServiceStateChange
title: IWTSProtocolManager::NotifyServiceStateChange
author: windows-driver-content
description: IWTSProtocolManager::NotifyServiceStateChange is no longer available. Instead, use IWRdsProtocolManager::NotifyServiceStateChange.
old-location: termserv\iwtsprotocolmanager_notifyservicestatechange.htm
old-project: TermServ
ms.assetid: 303a53b3-b297-486c-9422-706ec60441f2
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IWTSProtocolManager interface [Remote Desktop Services],NotifyServiceStateChange method, IWTSProtocolManager.NotifyServiceStateChange, IWTSProtocolManager::NotifyServiceStateChange, NotifyServiceStateChange, NotifyServiceStateChange method [Remote Desktop Services], NotifyServiceStateChange method [Remote Desktop Services],IWTSProtocolManager interface, termserv.iwtsprotocolmanager_notifyservicestatechange, wtsprotocol/IWTSProtocolManager::NotifyServiceStateChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wtsprotocol.h
api_name:
-	IWTSProtocolManager.NotifyServiceStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolManager::NotifyServiceStateChange


## -description


<p class="CCE_Message">[<b>IWTSProtocolManager::NotifyServiceStateChange</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/32b2a05a-d5de-4f2f-bcaa-587cf22aa5c5">IWRdsProtocolManager::NotifyServiceStateChange</a>.]

Notifies the protocol provider that the state of the Remote Desktop Services service is changing.


## -parameters




### -param pTSServiceStateChange [in]

A pointer to a <a href="https://msdn.microsoft.com/5f4469f5-5a64-4292-bbe6-cc030f1421f5">WTS_SERVICE_STATE</a> structure that specifies 
whether the service is starting, stopping, or changing its drain state.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/a54bdb46-b18b-4a6d-90fc-75947f6dd191">IWTSProtocolManager</a>
 

 

