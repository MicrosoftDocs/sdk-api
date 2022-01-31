---
UID: NE:msclus.CLUS_FLAGS
title: CLUS_FLAGS (msclus.h)
description: Identifies the resource or group as a core resource.
helpviewer_keywords: ["CLUS_FLAGS","CLUS_FLAGS enumeration [Failover Cluster]","CLUS_FLAG_CORE","_CLUS_FLAGS","_CLUS_FLAGS enumeration [Failover Cluster]","clusapi/CLUS_FLAGS","clusapi/CLUS_FLAG_CORE","clusapi/_CLUS_FLAGS","msclus/CLUS_FLAGS","msclus/CLUS_FLAG_CORE","msclus/_CLUS_FLAGS","mscs.clus_flags"]
old-location: mscs\clus_flags.htm
tech.root: MsCS
ms.assetid: 54d00b1c-cef7-4310-8c10-743ee7086979
ms.date: 12/05/2018
ms.keywords: CLUS_FLAGS, CLUS_FLAGS enumeration [Failover Cluster], CLUS_FLAG_CORE, _CLUS_FLAGS, _CLUS_FLAGS enumeration [Failover Cluster], clusapi/CLUS_FLAGS, clusapi/CLUS_FLAG_CORE, clusapi/_CLUS_FLAGS, msclus/CLUS_FLAGS, msclus/CLUS_FLAG_CORE, msclus/_CLUS_FLAGS, mscs.clus_flags
req.header: msclus.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
req.typenames: CLUS_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CLUS_FLAGS
 - msclus/CLUS_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
 - MsClus.h
api_name:
 - CLUS_FLAGS
---

# CLUS_FLAGS enumeration


## -description

Identifies the resource or group as a 
     <a href="/previous-versions/windows/desktop/mscs/core-resources">core resource</a>.

## -enum-fields

### -field CLUS_FLAG_CORE:0x1

Identifies <a href="/previous-versions/windows/desktop/mscs/core-resources">core resources</a> or the cluster group that 
       contains core resources. The 
       <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a> function with the 
       <a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-flags">CLUSCTL_RESOURCE_GET_FLAGS</a> control 
       code can retrieve the flags that are set for a resource.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/clusctl-resource-get-flags">CLUSCTL_RESOURCE_GET_FLAGS</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterresourcecontrol">ClusterResourceControl</a>
