---
UID: NF:wtsprotocol.IWTSProtocolManager.NotifySessionOfServiceStop
title: IWTSProtocolManager::NotifySessionOfServiceStop
author: windows-sdk-content
description: IWTSProtocolManager::NotifySessionOfServiceStop is no longer available. Instead, use IWRdsProtocolManager::NotifySessionOfServiceStop.
old-location: termserv\iwtsprotocolmanager_notifysessionofservicestop.htm
old-project: termserv
ms.assetid: cdad7006-4cd5-4ea3-84a3-f3cdeb57befa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWTSProtocolManager interface [Remote Desktop Services],NotifySessionOfServiceStop method, IWTSProtocolManager.NotifySessionOfServiceStop, IWTSProtocolManager::NotifySessionOfServiceStop, NotifySessionOfServiceStop, NotifySessionOfServiceStop method [Remote Desktop Services], NotifySessionOfServiceStop method [Remote Desktop Services],IWTSProtocolManager interface, termserv.iwtsprotocolmanager_notifysessionofservicestop, wtsprotocol/IWTSProtocolManager::NotifySessionOfServiceStop
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolManager.NotifySessionOfServiceStop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolManager::NotifySessionOfServiceStop


## -description


<p class="CCE_Message">[<b>IWTSProtocolManager::NotifySessionOfServiceStop</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/acf52eb0-d8f8-4257-9c2c-e9345c0f1b7f">IWRdsProtocolManager::NotifySessionOfServiceStop</a>.]

Notifies the protocol provider that the Remote Desktop Services service has stopped for a given session.


## -parameters




### -param SessionId [in]

A pointer to a <a href="https://msdn.microsoft.com/fe0714ec-c670-40b7-9808-2171abae79a8">WTS_SESSION_ID</a> structure that uniquely identifies the session.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/a54bdb46-b18b-4a6d-90fc-75947f6dd191">IWTSProtocolManager</a>
 

 

