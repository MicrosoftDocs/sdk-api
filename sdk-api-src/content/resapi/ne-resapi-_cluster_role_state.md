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

# _CLUSTER_ROLE_STATE enumeration


## -description


Defines the potential return values for the <a href="https://msdn.microsoft.com/582992ca-9381-4673-8fe8-835b50047f51">ResUtilGetClusterRoleState</a> function.


## -enum-fields




### -field ClusterRoleUnknown

It is unknown whether or not the role is clustered.


### -field ClusterRoleClustered

The role is clustered.


### -field ClusterRoleUnclustered

The role is not clustered.


## -see-also




<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>



<a href="https://msdn.microsoft.com/582992ca-9381-4673-8fe8-835b50047f51">ResUtilGetClusterRoleState</a>
 

 

