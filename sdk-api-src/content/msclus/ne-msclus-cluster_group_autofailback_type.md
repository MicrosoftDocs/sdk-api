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

# CLUSTER_GROUP_AUTOFAILBACK_TYPE enumeration


## -description


Used by the 
    <a href="https://msdn.microsoft.com/cd06c375-2684-4943-8587-692e655b44a2">AutoFailbackType</a> group 
    <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common property</a> to specify whether the group should be 
    failed back to the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> identified as its preferred owner when that 
    node comes back online following a <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">failover</a>.


## -enum-fields




### -field ClusterGroupPreventFailback

Prevents <a href="https://msdn.microsoft.com/dcb53180-86bf-4cba-bf93-9c19cbc127b8">failback</a>.


### -field ClusterGroupAllowFailback

Allows failback (requires a preferred owners list for the group).


### -field ClusterGroupFailbackTypeCount

Defines a maximum group property value. It is not supported by the 
       <a href="https://msdn.microsoft.com/cd06c375-2684-4943-8587-692e655b44a2">AutoFailbackType</a> group property.


## -see-also




<a href="https://msdn.microsoft.com/cd06c375-2684-4943-8587-692e655b44a2">AutoFailbackType</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common property</a>
 

 

