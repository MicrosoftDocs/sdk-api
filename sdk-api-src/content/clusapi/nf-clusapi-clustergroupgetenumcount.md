---
UID: NF:clusapi.ClusterGroupGetEnumCount
title: ClusterGroupGetEnumCount function (clusapi.h)
description: Returns the number of cluster objects associated with a group enumeration handle.
helpviewer_keywords: ["ClusterGroupGetEnumCount","ClusterGroupGetEnumCount function [Failover Cluster]","PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT","PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT function [Failover Cluster]","_wolf_clustergroupgetenumcount","clusapi/ClusterGroupGetEnumCount","clusapi/PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT","mscs.clustergroupgetenumcount"]
old-location: mscs\clustergroupgetenumcount.htm
tech.root: MsCS
ms.assetid: 068cd55e-4220-447c-bf2f-a515503b7cc9
ms.date: 12/05/2018
ms.keywords: ClusterGroupGetEnumCount, ClusterGroupGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT function [Failover Cluster], _wolf_clustergroupgetenumcount, clusapi/ClusterGroupGetEnumCount, clusapi/PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT, mscs.clustergroupgetenumcount
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ClusterGroupGetEnumCount
 - clusapi/ClusterGroupGetEnumCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterGroupGetEnumCount
---

# ClusterGroupGetEnumCount function


## -description

Returns the number of <a href="/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> associated with a 
    <a href="/previous-versions/windows/desktop/mscs/groups">group</a> enumeration handle. The <b>PCLUSAPI_CLUSTER_GROUP_GET_ENUM_COUNT</b> type defines a pointer to this function.

## -parameters

### -param hGroupEnum [in]

Handle to a group enumeration. This handle is obtained from 
      <a href="/windows/win32/api/clusapi/nf-clusapi-clustergroupopenenum">ClusterGroupOpenEnum</a>. A valid handle is 
      required. This parameter cannot be <b>NULL</b>.

## -returns

<b>ClusterGroupGetEnumCount</b> returns the 
       number of objects associated with the enumeration handle.