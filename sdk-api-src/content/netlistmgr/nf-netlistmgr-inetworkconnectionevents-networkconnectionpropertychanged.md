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

# INetworkConnectionEvents::NetworkConnectionPropertyChanged


## -description


The <b>NetworkConnectionPropertyChanged</b> method notifies a client when property change events related to a specific network connection occur.


## -parameters




### -param connectionId [in]

A GUID that identifies the network connection  on which the event occurred.


### -param flags






#### - fFlags [in]

The <a href="https://msdn.microsoft.com/75cc1876-e6e0-4c39-a0af-5c47e7501c98">NLM_CONNECTION_PROPERTY_CHANGE</a> flags for this connection.


## -returns



Returns S_OK if the method succeeds.




## -see-also




<a href="https://msdn.microsoft.com/339f23ee-583d-4623-ad43-00b4fd4395ad">INetworkConnectionEvents</a>



<a href="https://msdn.microsoft.com/75cc1876-e6e0-4c39-a0af-5c47e7501c98">NLM_CONNECTION_PROPERTY_CHANGE</a>
 

 

