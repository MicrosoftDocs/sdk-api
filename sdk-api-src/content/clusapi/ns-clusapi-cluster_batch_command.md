---
UID: NS:clusapi._CLUSTER_BATCH_COMMAND
title: CLUSTER_BATCH_COMMAND (clusapi.h)
description: Represents the order in which current batch command data is sent to the ClusterRegBatchReadCommand function.
helpviewer_keywords: ["CLUSREG_CREATE_KEY","CLUSREG_DELETE_KEY","CLUSREG_DELETE_VALUE","CLUSREG_SET_VALUE","CLUSREG_VALUE_DELETED","CLUSTER_BATCH_COMMAND","CLUSTER_BATCH_COMMAND structure [Failover Cluster]","clusapi/CLUSTER_BATCH_COMMAND","mscs.cluster_batch_command"]
old-location: mscs\cluster_batch_command.htm
tech.root: MsCS
ms.assetid: 31f8e255-80c8-4381-a8f3-0d48a3831a89
ms.date: 12/05/2018
ms.keywords: CLUSREG_CREATE_KEY, CLUSREG_DELETE_KEY, CLUSREG_DELETE_VALUE, CLUSREG_SET_VALUE, CLUSREG_VALUE_DELETED, CLUSTER_BATCH_COMMAND, CLUSTER_BATCH_COMMAND structure [Failover Cluster], clusapi/CLUSTER_BATCH_COMMAND, mscs.cluster_batch_command
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
req.typenames: CLUSTER_BATCH_COMMAND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_BATCH_COMMAND
 - clusapi/_CLUSTER_BATCH_COMMAND
 - CLUSTER_BATCH_COMMAND
 - clusapi/CLUSTER_BATCH_COMMAND
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
 - CLUSTER_BATCH_COMMAND
---

# CLUSTER_BATCH_COMMAND structure


## -description

Represents the order in which current batch command data is sent to the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregbatchreadcommand">ClusterRegBatchReadCommand</a> 
    function. Values in the 
    <b>CLUSTER_BATCH_COMMAND</b> structure are identical to 
    parameters passed to the 
    <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregbatchaddcommand">ClusterRegBatchAddCommand</a> function. The only 
    difference is that for <b>CLUSREG_DELETE_VALUE</b>, the <b>dwOptions</b>, 
    <b>lpData</b>, and <b>cbData</b> members are set to the value being 
    deleted, similar to the <b>CLUSREG_SET_VALUE</b> command.

## -struct-fields

### -field Command

A command that is supported by this API and taken from the 
       <a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_reg_command">CLUSTER_REG_COMMAND</a> enumeration. The possible 
       commands are as follows.



#### CLUSREG_SET_VALUE (1)

Sets a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or (if not 
         provided) relative to a key passed into the 
         <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatebatch">ClusterRegCreateBatch</a> function.



#### CLUSREG_CREATE_KEY (2)

Creates a specified cluster registry key if it does not exist, or opens an existing one.



#### CLUSREG_DELETE_KEY (3)

Deletes a key with all values and nested subkeys.  No commands that operate on values can follow 
         <b>CLUSREG_DELETE_KEY</b> until <b>CLUS_REG_CREATE_KEY</b> is 
         added.



#### CLUSREG_DELETE_VALUE (4)

Deletes a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or (if 
         not provided) relative to a key passed into the 
         <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatebatch">ClusterRegCreateBatch</a> function.



#### CLUSREG_VALUE_DELETED (6)

Indicates whether a  specific cluster registry value has been deleted or if the data of that cluster 
         registry value has been changed. This command is returned only through a batch update notification port.

### -field dwOptions

If the <b>Command</b> member takes either the 
       <b>CLUSREG_SET_VALUE</b> command or the <b>CLUSREG_DELETE_VALUE</b> 
       command, then this member takes one of the standard 
       <a href="/windows/desktop/SysInfo/registry-value-types">registry value types</a>. If not, then 
       <b>Command</b> is set to 0.

### -field wzName

The name of the value or key relative to the command issued by <b>Command</b>.

### -field lpData

A pointer to the data relative to the command issued by <b>Command</b>. The value of this 
       member is <b>NULL</b> for all the commands except the 
       <b>CLUSREG_SET_VALUE</b> and <b>CLUSREG_DELETE_VALUE</b> 
       commands.

### -field cbData

The count, in bytes, of the data relative to the command issued by <b>Command</b>. The 
       value of this member is 0 for all the commands except the <b>CLUSREG_SET_VALUE</b> and 
       <b>CLUSREG_DELETE_VALUE</b> commands.

## -remarks

The <b>wzName</b> and <b>lpData</b> pointers are valid until the batch 
     notification is closed via the 
     <a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregbatchclosenotification">ClusterRegBatchCloseNotification</a> 
     function.

## -see-also

<a href="/windows/desktop/api/clusapi/ne-clusapi-cluster_reg_command">CLUSTER_REG_COMMAND</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregbatchaddcommand">ClusterRegBatchAddCommand</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregbatchclosenotification">ClusterRegBatchCloseNotification</a>



<a href="/windows/desktop/api/clusapi/nf-clusapi-clusterregbatchreadcommand">ClusterRegBatchReadCommand</a>



<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatebatch">ClusterRegCreateBatch</a>



<a href="/previous-versions/windows/desktop/mscs/cluster-structures">Failover Cluster Structures</a>