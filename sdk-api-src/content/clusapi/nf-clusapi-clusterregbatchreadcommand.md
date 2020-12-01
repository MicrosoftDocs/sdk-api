---
UID: NF:clusapi.ClusterRegBatchReadCommand
title: ClusterRegBatchReadCommand function (clusapi.h)
description: Reads a command from a batch notification.
helpviewer_keywords: ["ClusterRegBatchReadCommand","ClusterRegBatchReadCommand function [Failover Cluster]","clusapi/ClusterRegBatchReadCommand","mscs.clusterregbatchreadcommand"]
old-location: mscs\clusterregbatchreadcommand.htm
tech.root: MsCS
ms.assetid: a1a7abc5-f306-4664-bb53-e54c6ee1051e
ms.date: 12/05/2018
ms.keywords: ClusterRegBatchReadCommand, ClusterRegBatchReadCommand function [Failover Cluster], clusapi/ClusterRegBatchReadCommand, mscs.clusterregbatchreadcommand
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
 - ClusterRegBatchReadCommand
 - clusapi/ClusterRegBatchReadCommand
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
 - ClusterRegBatchReadCommand
---

# ClusterRegBatchReadCommand function


## -description

Reads a command from a batch notification.

## -parameters

### -param hBatchNotification [in]

A handle to the batch notification.

### -param pBatchCommand [out]

Pointer to a <a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_batch_command">CLUSTER_BATCH_COMMAND</a> structure 
       that will be filled with information about the command on successful return.

## -returns

The function returns one of the following 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

The <b>PCLUSTER_REG_GET_BATCH_NOTIFICATION</b> type defines a pointer to this 
     function.

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_batch_command">CLUSTER_BATCH_COMMAND</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-registry-access-functions">Cluster Registry Access Functions</a>