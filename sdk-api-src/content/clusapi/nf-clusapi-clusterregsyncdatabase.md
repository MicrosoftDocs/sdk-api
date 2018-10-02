---
UID: NF:clusapi.ClusterRegSyncDatabase
title: ClusterRegSyncDatabase function
author: windows-sdk-content
description: Synchronizes the Cluster Database with a cluster.
old-location: mscs\clusterregsyncdatabase.htm
tech.root: MsCS
ms.assetid: 90A66286-F17D-40AD-B0CB-6E02C1E1709A
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ClusterRegSyncDatabase, ClusterRegSyncDatabase function [Failover Cluster], PCLUSAPI_CLUSTER_REG_SYNC_DATABASE, PCLUSAPI_CLUSTER_REG_SYNC_DATABASE function [Failover Cluster], clusapi/ClusterRegSyncDatabase, clusapi/PCLUSAPI_CLUSTER_REG_SYNC_DATABASE, mscs.clusterregsyncdatabase
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# ClusterRegSyncDatabase function


## -description


Synchronizes the <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">Cluster Database</a> with a cluster.


## -parameters




### -param hCluster

A handle to the cluster to synchronize with the cluster database.


### -param flags

This parameter is reserved for future use.


## -returns



If the operation succeeds, returns <b>ERROR_SUCCESS</b> (0); otherwise, returns a system error code.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>
 

 

