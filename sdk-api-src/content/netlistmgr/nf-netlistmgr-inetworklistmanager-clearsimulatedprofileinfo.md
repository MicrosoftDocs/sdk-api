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

# INetworkListManager::ClearSimulatedProfileInfo


## -description


Clears the connection profile values previously applied to the internet connection profile by <a href="https://msdn.microsoft.com/168501A6-F8B2-4635-97BB-538994074D2C">SetSimulatedProfileInfo</a>. The next internet connection query, via <a href="https://msdn.microsoft.com/30d85516-1150-45a1-8941-a299019897d6">GetInternetConnectionProfile</a>, will use system information.


## -parameters






## -returns



Returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/a9f76b6a-ea15-47b7-a4ef-14ea60b7810d">INetworkListManager</a>



<a href="https://msdn.microsoft.com/168501A6-F8B2-4635-97BB-538994074D2C">SetSimulatedProfileInfo</a>
 

 

