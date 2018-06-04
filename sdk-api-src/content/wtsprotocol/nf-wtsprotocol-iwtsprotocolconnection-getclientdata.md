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

# IWTSProtocolConnection::GetClientData


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::GetClientData</b> 
    is no longer available for use as of Windows Server 2012. Instead, use 
    <a href="https://msdn.microsoft.com/4005ff92-56ea-46ae-a546-e08a80303ef5">IWRdsProtocolConnection::GetClientData</a>.]

Requests client settings from the protocol.


## -parameters




### -param pClientData [out]

A pointer to a <a href="https://msdn.microsoft.com/a8e0fcbd-4f5c-4692-9bb0-aaa00465acf0">WTS_CLIENT_DATA</a> structure that contains the client settings.


## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

