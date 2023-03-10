---
UID: NS:clusapi._CLUSTER_READ_BATCH_COMMAND
title: CLUSTER_READ_BATCH_COMMAND (clusapi.h)
description: Represents a result for a single command in a read batch.
helpviewer_keywords: ["CLUSREG_READ_ERROR","CLUSREG_READ_VALUE","CLUSTER_READ_BATCH_COMMAND","CLUSTER_READ_BATCH_COMMAND structure [Failover Cluster]","PCLUSTER_READ_BATCH_COMMAND","PCLUSTER_READ_BATCH_COMMAND structure pointer [Failover Cluster]","clusapi/CLUSTER_READ_BATCH_COMMAND","clusapi/PCLUSTER_READ_BATCH_COMMAND","mscs.cluster_read_batch_command"]
old-location: mscs\cluster_read_batch_command.htm
tech.root: MsCS
ms.assetid: BE7D4B99-27C0-4CAA-BFDC-669737E17D86
ms.date: 12/05/2018
ms.keywords: CLUSREG_READ_ERROR, CLUSREG_READ_VALUE, CLUSTER_READ_BATCH_COMMAND, CLUSTER_READ_BATCH_COMMAND structure [Failover Cluster], PCLUSTER_READ_BATCH_COMMAND, PCLUSTER_READ_BATCH_COMMAND structure pointer [Failover Cluster], clusapi/CLUSTER_READ_BATCH_COMMAND, clusapi/PCLUSTER_READ_BATCH_COMMAND, mscs.cluster_read_batch_command
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: CLUSTER_READ_BATCH_COMMAND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_READ_BATCH_COMMAND
 - clusapi/_CLUSTER_READ_BATCH_COMMAND
 - CLUSTER_READ_BATCH_COMMAND
 - clusapi/CLUSTER_READ_BATCH_COMMAND
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
 - CLUSTER_READ_BATCH_COMMAND
---

# CLUSTER_READ_BATCH_COMMAND structure


## -description

Represents a result for a single command in a read batch.

## -struct-fields

### -field Command

The command result status, which can be one of these values.



#### CLUSREG_READ_VALUE (8)

The result structure has content for the requested value. The <b>dwOptions</b> member is set to the registry value type.



#### CLUSREG_READ_ERROR (9)

The value was missing, or another error occurred during read. The <b>dwOptions</b> member contains the actual error type.

### -field dwOptions

The registry value type or the read error type, depending on the <i>Command</i> result.

### -field wzSubkeyName

The name of the key requested in the read command.

### -field wzValueName

The name of the value requested in the read command.

### -field lpData

A pointer to value data.

### -field cbData

The count, in bytes, of the <i>lpData</i> value data.

## -remarks

The pointers in the <b>CLUSTER_READ_BATCH_COMMAND</b> structure are valid until the read batch result handle is closed by the <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatchreply">ClusterRegCloseReadBatchReply</a> function.

Errors from read commands are independent from each other.

## -see-also

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregclosereadbatchreply">ClusterRegCloseReadBatchReply</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregreadbatchreplynextcommand">ClusterRegReadBatchReplyNextCommand</a>