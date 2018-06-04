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

# PCLUSAPI_GET_CLUSTER_NETWORK_STATE callback function


## -description


Returns 
    the current state of a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>. The <b>PCLUSAPI_GET_CLUSTER_NETWORK_STATE</b> type defines a pointer to this function.


## -parameters




### -param hNetwork [in]

Handle to the network for which state information should be returned.


## -returns



<i>GetClusterNetworkState</i> returns the current 
       state of the network, which is represented by one of the following values enumerated by the 
       <a href="https://msdn.microsoft.com/1a9e3ff0-eb5a-4a2e-ae19-e70213dc1a4a">CLUSTER_NETWORK_STATE</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/1a9e3ff0-eb5a-4a2e-ae19-e70213dc1a4a">CLUSTER_NETWORK_STATE</a>



<a href="https://msdn.microsoft.com/a888ca91-e56f-42bc-81c5-9235c6fd5172">OpenClusterNetwork</a>
 

 

