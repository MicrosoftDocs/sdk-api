---
UID: NF:clusapi.ClusterNodeGetEnumCount
title: ClusterNodeGetEnumCount function (clusapi.h)
description: Returns the number of cluster objects associated with a node enumeration handle.
helpviewer_keywords: ["ClusterNodeGetEnumCount","ClusterNodeGetEnumCount function [Failover Cluster]","PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT","PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT function [Failover Cluster]","_wolf_clusternodegetenumcount","clusapi/ClusterNodeGetEnumCount","clusapi/PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT","mscs.clusternodegetenumcount"]
old-location: mscs\clusternodegetenumcount.htm
tech.root: MsCS
ms.assetid: bec31b84-a4fd-48a3-b465-ceebb1f61028
ms.date: 12/05/2018
ms.keywords: ClusterNodeGetEnumCount, ClusterNodeGetEnumCount function [Failover Cluster], PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT, PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT function [Failover Cluster], _wolf_clusternodegetenumcount, clusapi/ClusterNodeGetEnumCount, clusapi/PCLUSAPI_CLUSTER_NODE_GET_ENUM_COUNT, mscs.clusternodegetenumcount
f1_keywords:
- clusapi/ClusterNodeGetEnumCount
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ClusAPI.dll
- ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
- ClusterNodeGetEnumCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterNodeGetEnumCount function


## -description


Returns the number of  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-objects">cluster objects</a> associated with a  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a> enumeration handle.


## -parameters




### -param hNodeEnum [in]

Handle to a node enumeration. This handle is obtained from  <a href="https://docs.microsoft.com/windows/desktop/api/clusapi/nf-clusapi-clusternodeopenenum">ClusterNodeOpenEnum</a>. A valid handle is required. This parameter cannot be <b>NULL</b>.


## -returns



<b>ClusterNodeGetEnumCount</b> returns the number of objects associated with the enumeration handle.



