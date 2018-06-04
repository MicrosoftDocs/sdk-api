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

# IWTSProtocolConnection::CreateVirtualChannel


## -description


<p class="CCE_Message">[<b>IWTSProtocolConnection::CreateVirtualChannel</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/c0302081-06af-44af-a9ed-936d705e711b">IWRdsProtocolConnection::CreateVirtualChannel</a>.]

Creates a static or dynamic virtual channel.


## -parameters




### -param szEndpointName [in]

A string value that contains the endpoint data that uniquely identifies the connection.


### -param bStatic [in]

A Boolean value that specifies whether the virtual channel is static or dynamic. A value of <b>TRUE</b> specifies a static channel.


### -param RequestedPriority [in]

An integer that contains the priority.


### -param phChannel [out]

A pointer to the channel handle.


## -remarks



Virtual channels are software extensions that can be created to enhance a Remote Desktop Services application. Examples include support for additional hardware or additions to the functionality provided by a given protocol. For more information, see <a href="https://msdn.microsoft.com/f7bdebec-ecc3-4f28-9327-f0d2f169c142">Remote Desktop Services Virtual 
      Channels</a>.




## -see-also




<a href="https://msdn.microsoft.com/584a6874-0df4-480e-a10a-4b603643870e">IWTSProtocolConnection</a>
 

 

