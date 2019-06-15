---
UID: NF:clusapi.ClusterRegSyncDatabase
title: ClusterRegSyncDatabase function (clusapi.h)
author: windows-sdk-content
description: Synchronizes the Cluster Database with a cluster.
old-location: mscs\clusterregsyncdatabase.htm
tech.root: MsCS
ms.assetid: 90A66286-F17D-40AD-B0CB-6E02C1E1709A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ClusterRegSyncDatabase, ClusterRegSyncDatabase function [Failover Cluster], PCLUSAPI_CLUSTER_REG_SYNC_DATABASE, PCLUSAPI_CLUSTER_REG_SYNC_DATABASE function [Failover Cluster], clusapi/ClusterRegSyncDatabase, clusapi/PCLUSAPI_CLUSTER_REG_SYNC_DATABASE, mscs.clusterregsyncdatabase
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
api_name:
 - ClusterRegSyncDatabase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ClusterRegSyncDatabase function


## -description


Synchronizes the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-database">Cluster Database</a> with a cluster.


## -parameters




### -param hCluster

A handle to the cluster to synchronize with the cluster database.


### -param flags

This parameter is reserved for future use.


## -returns



If the operation succeeds, returns <b>ERROR_SUCCESS</b> (0); otherwise, returns a system error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>
 

 

