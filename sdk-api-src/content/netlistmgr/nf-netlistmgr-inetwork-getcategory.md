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

# INetwork::GetCategory


## -description


The <b>GetCategory</b> method returns the category of a network.


## -parameters




### -param pCategory [out]

Pointer to a <a href="https://msdn.microsoft.com/1bc9720f-7b31-4a09-8bce-a6281ca9b9c4">NLM_NETWORK_CATEGORY</a> enumeration value that specifies the category information for the network.


## -returns



Returns S_OK if the method succeeds.




## -remarks



The private or public network categories must never be used to assume  which Windows Firewall ports are open, as the user can change the default settings of these categories. Instead, Windows Firewall APIs should be called to ensure the ports that the required ports are open.




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>



<a href="https://msdn.microsoft.com/1bc9720f-7b31-4a09-8bce-a6281ca9b9c4">NLM_NETWORK_CATEGORY</a>
 

 

