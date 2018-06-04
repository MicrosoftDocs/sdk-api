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

# INetworkEvents::NetworkPropertyChanged


## -description


The <b>NetworkPropertyChanged</b> method is called when a network property change is detected.


## -parameters




### -param networkId




### -param flags






#### - fFlags [in]


<a href="https://msdn.microsoft.com/04c96793-f6a8-418b-a8d4-65e8df77933c">NLM_NETWORK_PROPERTY_CHANGE</a> enumeration value that specifies the network property that changed.


#### - gdNetworkId [in]

GUID that specifies the network on which this event occurred.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/75cc6efb-dd1b-40b6-84fe-5ba7c244cd72">INetworkEvents</a>



<a href="https://msdn.microsoft.com/04c96793-f6a8-418b-a8d4-65e8df77933c">NLM_NETWORK_PROPERTY_CHANGE</a>
 

 

