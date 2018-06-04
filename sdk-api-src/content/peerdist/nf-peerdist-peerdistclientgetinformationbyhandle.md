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

# PeerDistClientGetInformationByHandle function


## -description


The <b>PeerDistClientGetInformationByHandle</b> function retrieves additional information from the Peer Distribution service for a specific content handle.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by the <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a> function.


### -param hContentHandle [in]

A <b>PEERDIST_CONTENT_HANDLE</b> returned by the <a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a> function.


### -param PeerDistClientInfoClass [in]

A value from the <a href="https://msdn.microsoft.com/28391dc5-ec89-44d9-acac-b7ff3868e542">PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS</a> enumeration that indicates the information to retrieve.


### -param dwBufferSize

The size, in bytes, of the buffer for the <i>lpInformation</i> parameter.


### -param lpInformation [out]

A buffer for the returned information. The format of this information depends on the value of the <i>PeerDistClientInfoClass</i> parameter.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.




## -see-also




<a href="https://msdn.microsoft.com/28391dc5-ec89-44d9-acac-b7ff3868e542">PEERDIST_CLIENT_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/bf9d4eb2-e939-42c6-8d71-669a949ca77a">PeerDistClientOpenContent</a>



<a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>
 

 

