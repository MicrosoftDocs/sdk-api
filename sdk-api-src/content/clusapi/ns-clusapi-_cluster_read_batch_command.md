---
UID: NS:clusapi._CLUSTER_READ_BATCH_COMMAND
title: "_CLUSTER_READ_BATCH_COMMAND"
author: windows-sdk-content
description: Represents a result for a single command in a read batch.
old-location: mscs\cluster_read_batch_command.htm
tech.root: MsCS
ms.assetid: BE7D4B99-27C0-4CAA-BFDC-669737E17D86
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CLUSREG_READ_ERROR, CLUSREG_READ_VALUE, CLUSTER_READ_BATCH_COMMAND, CLUSTER_READ_BATCH_COMMAND structure [Failover Cluster], PCLUSTER_READ_BATCH_COMMAND, PCLUSTER_READ_BATCH_COMMAND structure pointer [Failover Cluster], _CLUSTER_READ_BATCH_COMMAND, clusapi/CLUSTER_READ_BATCH_COMMAND, clusapi/PCLUSTER_READ_BATCH_COMMAND, mscs.cluster_read_batch_command
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_READ_BATCH_COMMAND
product: Windows
targetos: Windows
req.typenames: CLUSTER_READ_BATCH_COMMAND
req.redist: 
---

# _CLUSTER_READ_BATCH_COMMAND structure


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



The pointers in the <b>CLUSTER_READ_BATCH_COMMAND</b> structure are valid until the read batch result handle is closed by the <a href="https://msdn.microsoft.com/en-us/library/Hh706742(v=VS.85).aspx">ClusterRegCloseReadBatchReply</a> function.

Errors from read commands are independent from each other.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh706742(v=VS.85).aspx">ClusterRegCloseReadBatchReply</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706745(v=VS.85).aspx">ClusterRegReadBatchReplyNextCommand</a>
 

 

