---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWTSProtocolConnection::SendPolicyData


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::SendPolicyData</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/80292d9b-fced-4726-8f83-5ba355df06a2">IWRdsProtocolManager::NotifySettingsChange</a>.]

Sends computer policy settings to the custom protocol. These settings are a combination of listener policies and Group Policy settings.


## -parameters




### -param pPolicyData [in]

A pointer to a <a href="https://msdn.microsoft.com/407de671-f6e3-407e-9c97-11ea9ac8bdde">WTS_POLICY_DATA</a> structure that contains computer policy settings.


## -remarks



The <b>SendPolicyData</b> method is the second method called by the Remote Desktop Services service during a connection sequence.  The protocol must call the <a href="https://msdn.microsoft.com/a1289aca-bcf6-4fd2-a288-d401bece005d">OnReady</a> method after this method is called, or the connection is dropped. 




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

