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

# CLUSTER_QUORUM_VALUE enumeration


## -description


Enumerates values returned by the 
    <a href="https://msdn.microsoft.com/7ef06c95-8d9d-4b87-a6d8-d6a2d49523ee">ClusterControl</a> function with the 
    <a href="https://msdn.microsoft.com/4987c8c1-7f5a-4b4a-8fba-55457922b641">CLUSCTL_CLUSTER_CHECK_VOTER_DOWN</a> or the 
    <a href="https://msdn.microsoft.com/e87d5598-01f5-4d33-aa8c-e9c059cb9716">CLUSCTL_CLUSTER_CHECK_VOTER_EVICT</a> 
    control codes.


## -enum-fields




### -field CLUSTER_QUORUM_MAINTAINED

The quorum will be maintained.


### -field CLUSTER_QUORUM_LOST

The quorum will be lost.


## -see-also




<a href="https://msdn.microsoft.com/4987c8c1-7f5a-4b4a-8fba-55457922b641">CLUSCTL_CLUSTER_CHECK_VOTER_DOWN</a>



<a href="https://msdn.microsoft.com/e87d5598-01f5-4d33-aa8c-e9c059cb9716">CLUSCTL_CLUSTER_CHECK_VOTER_EVICT</a>



<a href="https://msdn.microsoft.com/7ef06c95-8d9d-4b87-a6d8-d6a2d49523ee">ClusterControl</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

