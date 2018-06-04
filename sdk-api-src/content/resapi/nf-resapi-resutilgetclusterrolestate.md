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

# ResUtilGetClusterRoleState function


## -description


Determines whether or not a specific role has been assigned to a cluster.


## -parameters




### -param hCluster [in]

The handle of the queried cluster.


### -param eClusterRole [in]

The role the cluster was queried about.  The possible values for this parameter are enumerators from the <a href="https://msdn.microsoft.com/65fc8a8f-0a9e-464c-b62a-d2e61431d927">CLUSTER_ROLE</a> enumeration.  The following values are valid.



#### ClusterRoleDHCP (0)

This enumerator represents the DHCP Service cluster role.



#### ClusterRoleDTC (1)

This enumerator represents the Distributed Transaction Coordinator cluster role.



#### ClusterRoleFileServer (2)

This enumerator represents the File Share cluster role.



#### ClusterRoleGenericApplication (3)

This enumerator represents the Generic Application cluster role.



#### ClusterRoleGenericScript (4)

This enumerator represents the Generic Script cluster role.



#### ClusterRoleGenericService (5)

This enumerator represents the Generic Service cluster role.



#### ClusterRoleISCSINameServer (6)

This enumerator represents the Microsoft iSNS cluster role.



#### ClusterRoleMSMQ (7)

This enumerator represents the Microsoft Message Queue cluster role.



#### ClusterRoleNFS (8)

This enumerator represents the NFS Share cluster role.



#### ClusterRolePrintServer (9)

This enumerator represents the Print Spooler cluster role.



#### ClusterRoleStandAloneNamespaceServer (10)

This enumerator represents a specialized File Share cluster role.



#### ClusterRoleVolumeShadowCopyServiceTask (11)

This enumerator represents the Volume Shadow Copy Service Task cluster role.



#### ClusterRoleWINS (12)

This enumerator represents the WINS Service cluster role.


## -returns



The possible return values for this function are enumerators from the  <a href="https://msdn.microsoft.com/21424e31-4eba-4ff9-95c1-0908827936df">CLUSTER_ROLE_STATE</a> enumeration.  The following values are valid.




## -see-also




<a href="https://msdn.microsoft.com/65fc8a8f-0a9e-464c-b62a-d2e61431d927">CLUSTER_ROLE</a>



<a href="https://msdn.microsoft.com/21424e31-4eba-4ff9-95c1-0908827936df">CLUSTER_ROLE_STATE</a>



<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 

