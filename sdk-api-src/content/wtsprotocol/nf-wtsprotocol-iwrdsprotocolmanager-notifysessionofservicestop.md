---
UID: NF:wtsprotocol.IWRdsProtocolManager.NotifySessionOfServiceStop
title: IWRdsProtocolManager::NotifySessionOfServiceStop
author: windows-sdk-content
description: Notifies the protocol provider that the Remote Desktop Services service has stopped for a given session.
old-location: termserv\iwrdsprotocolmanager_notifysessionofservicestop.htm
old-project: TermServ
ms.assetid: acf52eb0-d8f8-4257-9c2c-e9345c0f1b7f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWRdsProtocolManager interface [Remote Desktop Services],NotifySessionOfServiceStop method, IWRdsProtocolManager.NotifySessionOfServiceStop, IWRdsProtocolManager::NotifySessionOfServiceStop, NotifySessionOfServiceStop, NotifySessionOfServiceStop method [Remote Desktop Services], NotifySessionOfServiceStop method [Remote Desktop Services],IWRdsProtocolManager interface, termserv.iwrdsprotocolmanager_notifysessionofservicestop, wtsprotocol/IWRdsProtocolManager::NotifySessionOfServiceStop
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolManager.NotifySessionOfServiceStop
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWRdsProtocolManager::NotifySessionOfServiceStop


## -description


Notifies the protocol provider that the Remote Desktop Services service has stopped for a given session.


## -parameters




### -param SessionId [in]

A pointer to a <a href="https://msdn.microsoft.com/fe0714ec-c670-40b7-9808-2171abae79a8">WRDS_SESSION_ID</a> structure that uniquely identifies the session.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/626d579a-88a2-4f72-9d91-b27e517b4806">IWRdsProtocolManager</a>
 

 

