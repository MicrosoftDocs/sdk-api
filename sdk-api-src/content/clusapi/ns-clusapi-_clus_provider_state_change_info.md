---
UID: NS:clusapi._CLUS_PROVIDER_STATE_CHANGE_INFO
title: "_CLUS_PROVIDER_STATE_CHANGE_INFO"
author: windows-sdk-content
description: Contains data about the state of a provider resource.
old-location: mscs\clus_provider_state_change_info.htm
tech.root: mscs
ms.assetid: 53e25d02-6dfa-4a74-8ff3-01c868d2fd44
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PCLUS_PROVIDER_STATE_CHANGE_INFO, CLUS_PROVIDER_STATE_CHANGE_INFO, CLUS_PROVIDER_STATE_CHANGE_INFO structure [Failover Cluster], ClusterResourceFailed, ClusterResourceInherited, ClusterResourceOffline, ClusterResourceOfflinePending, ClusterResourceOnline, ClusterResourceOnlinePending, PCLUS_PROVIDER_STATE_CHANGE_INFO, PCLUS_PROVIDER_STATE_CHANGE_INFO structure pointer [Failover Cluster], _CLUS_PROVIDER_STATE_CHANGE_INFO, clusapi/CLUS_PROVIDER_STATE_CHANGE_INFO, clusapi/PCLUS_PROVIDER_STATE_CHANGE_INFO, mscs.clus_provider_state_change_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: clusapi.h
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
 - ClusAPI.h
api_name:
 - CLUS_PROVIDER_STATE_CHANGE_INFO
product: Windows
targetos: Windows
req.typenames: CLUS_PROVIDER_STATE_CHANGE_INFO, *PCLUS_PROVIDER_STATE_CHANGE_INFO
req.redist: 
---

# _CLUS_PROVIDER_STATE_CHANGE_INFO structure


## -description


Contains data about the state of a <a href="https://msdn.microsoft.com/en-us/library/Aa371816(v=VS.85).aspx">provider</a> resource.


## -struct-fields




### -field dwSize

The size of this structure including the provider name and the terminating null character.


### -field resourceState

An enumerator from the <a href="https://msdn.microsoft.com/en-us/library/Bb309168(v=VS.85).aspx">CLUSTER_RESOURCE_STATE</a> enumeration as its value.  The following are the possible values for this member.



#### ClusterResourceInherited (0)

The resource has been inherited.



#### ClusterResourceOnline (2)

The resource is operational and functioning normally.



#### ClusterResourceOffline (3)

The resource is not operational.



#### ClusterResourceFailed (4)

The resource has <a href="https://msdn.microsoft.com/en-us/library/Aa369590(v=VS.85).aspx">failed</a>.



#### ClusterResourceOnlinePending (129 (0x81))

The resource is in the process of coming online.



#### ClusterResourceOfflinePending (130 (0x82))

The resource is in the process of going offline.


### -field szProviderId

The globally unique ID of the provider resource. This value can also be passed to the <i>lpszResourceName</i> parameter of the <a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a> function instead of a resource's name.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309168(v=VS.85).aspx">CLUSTER_RESOURCE_STATE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369339(v=VS.85).aspx">Data Structures</a>



<a href="https://msdn.microsoft.com/c699cb00-b999-45b8-b9db-570150e1a65e">OpenClusterResource</a>
 

 

