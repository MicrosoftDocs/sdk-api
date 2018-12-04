---
UID: NE:resapi._CLUSTER_ROLE_STATE
title: "_CLUSTER_ROLE_STATE"
author: windows-sdk-content
description: Defines the potential return values for the ResUtilGetClusterRoleState function.
old-location: mscs\cluster_role_state.htm
tech.root: mscs
ms.assetid: 21424e31-4eba-4ff9-95c1-0908827936df
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CLUSTER_ROLE_STATE, CLUSTER_ROLE_STATE enumeration [Failover Cluster], ClusterRoleClustered, ClusterRoleUnclustered, ClusterRoleUnknown, _CLUSTER_ROLE_STATE, mscs.cluster_role_state, resapi/CLUSTER_ROLE_STATE, resapi/ClusterRoleClustered, resapi/ClusterRoleUnclustered, resapi/ClusterRoleUnknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ResApi.h
api_name:
 - CLUSTER_ROLE_STATE
product: Windows
targetos: Windows
req.typenames: CLUSTER_ROLE_STATE
req.redist: 
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
 

 

