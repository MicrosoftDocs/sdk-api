---
UID: NF:clusapi.CloseCluster
title: CloseCluster function (clusapi.h)
description: Closes a cluster handle.
helpviewer_keywords: ["CloseCluster","CloseCluster function [Failover Cluster]","PCLUSAPI_CLOSE_CLUSTER","PCLUSAPI_CLOSE_CLUSTER function [Failover Cluster]","_wolf_closecluster","clusapi/CloseCluster","clusapi/PCLUSAPI_CLOSE_CLUSTER","mscs.closecluster"]
old-location: mscs\closecluster.htm
tech.root: MsCS
ms.assetid: cf055fd6-b1e1-4262-b205-c7d926522450
ms.date: 12/05/2018
ms.keywords: CloseCluster, CloseCluster function [Failover Cluster], PCLUSAPI_CLOSE_CLUSTER, PCLUSAPI_CLOSE_CLUSTER function [Failover Cluster], _wolf_closecluster, clusapi/CloseCluster, clusapi/PCLUSAPI_CLOSE_CLUSTER, mscs.closecluster
req.header: clusapi.h
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
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CloseCluster
 - clusapi/CloseCluster
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-cluster-clusapi-l1-1-6.dll
 - ext-ms-win-cluster-clusapi-l1-1-5.dll
 - ext-ms-win-cluster-clusapi-l1-1-4.dll
 - ClusAPI.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
 - ext-ms-win-cluster-clusapi-l1-1-3.dll
api_name:
 - CloseCluster
---

# CloseCluster function


## -description

Closes a cluster handle. The <b>PCLUSAPI_CLOSE_CLUSTER</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Handle to the cluster to close.

## -returns

This function always returns <b>TRUE</b>.

## -remarks

Do not close a cluster handle if there are any object handles still in use that were obtained from the cluster 
    handle. After a cluster handle has been closed, all handles obtained from that handle are invalid.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/using-object-handles">Using Object Handles</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clusapi/nf-clusapi-createcluster">CreateCluster</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-opencluster">OpenCluster</a>