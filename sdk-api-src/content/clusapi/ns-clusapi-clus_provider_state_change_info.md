---
UID: NS:clusapi._CLUS_PROVIDER_STATE_CHANGE_INFO
title: CLUS_PROVIDER_STATE_CHANGE_INFO (clusapi.h)
description: Contains data about the state of a provider resource.
helpviewer_keywords: ["*PCLUS_PROVIDER_STATE_CHANGE_INFO","CLUS_PROVIDER_STATE_CHANGE_INFO","CLUS_PROVIDER_STATE_CHANGE_INFO structure [Failover Cluster]","ClusterResourceFailed","ClusterResourceInherited","ClusterResourceOffline","ClusterResourceOfflinePending","ClusterResourceOnline","ClusterResourceOnlinePending","PCLUS_PROVIDER_STATE_CHANGE_INFO","PCLUS_PROVIDER_STATE_CHANGE_INFO structure pointer [Failover Cluster]","clusapi/CLUS_PROVIDER_STATE_CHANGE_INFO","clusapi/PCLUS_PROVIDER_STATE_CHANGE_INFO","mscs.clus_provider_state_change_info"]
old-location: mscs\clus_provider_state_change_info.htm
tech.root: MsCS
ms.assetid: 53e25d02-6dfa-4a74-8ff3-01c868d2fd44
ms.date: 12/05/2018
ms.keywords: '*PCLUS_PROVIDER_STATE_CHANGE_INFO, CLUS_PROVIDER_STATE_CHANGE_INFO, CLUS_PROVIDER_STATE_CHANGE_INFO structure [Failover Cluster], ClusterResourceFailed, ClusterResourceInherited, ClusterResourceOffline, ClusterResourceOfflinePending, ClusterResourceOnline, ClusterResourceOnlinePending, PCLUS_PROVIDER_STATE_CHANGE_INFO, PCLUS_PROVIDER_STATE_CHANGE_INFO structure pointer [Failover Cluster], clusapi/CLUS_PROVIDER_STATE_CHANGE_INFO, clusapi/PCLUS_PROVIDER_STATE_CHANGE_INFO, mscs.clus_provider_state_change_info'
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
targetos: Windows
req.typenames: CLUS_PROVIDER_STATE_CHANGE_INFO, *PCLUS_PROVIDER_STATE_CHANGE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUS_PROVIDER_STATE_CHANGE_INFO
 - clusapi/_CLUS_PROVIDER_STATE_CHANGE_INFO
 - PCLUS_PROVIDER_STATE_CHANGE_INFO
 - clusapi/PCLUS_PROVIDER_STATE_CHANGE_INFO
 - CLUS_PROVIDER_STATE_CHANGE_INFO
 - clusapi/CLUS_PROVIDER_STATE_CHANGE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUS_PROVIDER_STATE_CHANGE_INFO
---

# CLUS_PROVIDER_STATE_CHANGE_INFO structure


## -description

Contains data about the state of a <a href="/previous-versions/windows/desktop/mscs/p-gly">provider</a> resource.

## -struct-fields

### -field dwSize

The size of this structure including the provider name and the terminating null character.

### -field resourceState

An enumerator from the <a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a> enumeration as its value.  The following are the possible values for this member.



#### ClusterResourceInherited (0)

The resource has been inherited.



#### ClusterResourceOnline (2)

The resource is operational and functioning normally.



#### ClusterResourceOffline (3)

The resource is not operational.



#### ClusterResourceFailed (4)

The resource has <a href="/previous-versions/windows/desktop/mscs/f-gly">failed</a>.



#### ClusterResourceOnlinePending (129 (0x81))

The resource is in the process of coming online.



#### ClusterResourceOfflinePending (130 (0x82))

The resource is in the process of going offline.

### -field szProviderId

The globally unique ID of the provider resource. This value can also be passed to the <i>lpszResourceName</i> parameter of the <a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a> function instead of a resource's name.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/ne-clusapi-cluster_resource_state">CLUSTER_RESOURCE_STATE</a>



<a href="/previous-versions/windows/desktop/mscs/data-structures">Data Structures</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-openclusterresource">OpenClusterResource</a>