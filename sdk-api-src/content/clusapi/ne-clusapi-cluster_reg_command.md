---
UID: NE:clusapi._CLUSTER_REG_COMMAND
title: CLUSTER_REG_COMMAND (clusapi.h)
description: Enumerates the possible cluster registry commands that a local node will perform when attempting to join a cluster.
helpviewer_keywords: ["CLUSREG_COMMAND_NONE","CLUSREG_CONDITION_EXISTS","CLUSREG_CONDITION_IS_EQUAL","CLUSREG_CONDITION_IS_GREATER_THAN","CLUSREG_CONDITION_IS_KEY_NOT_EXISTS","CLUSREG_CONDITION_IS_LESS_THAN","CLUSREG_CONDITION_IS_NOT_EQUAL","CLUSREG_CONDITION_KEY_EXISTS","CLUSREG_CONDITION_NOT_EXISTS","CLUSREG_CONTROL_COMMAND","CLUSREG_CREATE_KEY","CLUSREG_DELETE_KEY","CLUSREG_DELETE_VALUE","CLUSREG_LAST_COMMAND","CLUSREG_READ_ERROR","CLUSREG_READ_VALUE","CLUSREG_SET_KEY_SECURITY","CLUSREG_SET_VALUE","CLUSREG_VALUE_DELETED","CLUSTER_REG_COMMAND","CLUSTER_REG_COMMAND enumeration [Failover Cluster]","_CLUSTER_REG_COMMAND","_CLUSTER_REG_COMMAND enumeration [Failover Cluster]","clusapi/CLUSREG_COMMAND_NONE","clusapi/CLUSREG_CONDITION_EXISTS","clusapi/CLUSREG_CONDITION_IS_EQUAL","clusapi/CLUSREG_CONDITION_IS_GREATER_THAN","clusapi/CLUSREG_CONDITION_IS_KEY_NOT_EXISTS","clusapi/CLUSREG_CONDITION_IS_LESS_THAN","clusapi/CLUSREG_CONDITION_IS_NOT_EQUAL","clusapi/CLUSREG_CONDITION_KEY_EXISTS","clusapi/CLUSREG_CONDITION_NOT_EXISTS","clusapi/CLUSREG_CONTROL_COMMAND","clusapi/CLUSREG_CREATE_KEY","clusapi/CLUSREG_DELETE_KEY","clusapi/CLUSREG_DELETE_VALUE","clusapi/CLUSREG_LAST_COMMAND","clusapi/CLUSREG_READ_ERROR","clusapi/CLUSREG_READ_VALUE","clusapi/CLUSREG_SET_KEY_SECURITY","clusapi/CLUSREG_SET_VALUE","clusapi/CLUSREG_VALUE_DELETED","clusapi/CLUSTER_REG_COMMAND","clusapi/_CLUSTER_REG_COMMAND","msclus/CLUSREG_COMMAND_NONE","msclus/CLUSREG_CONDITION_EXISTS","msclus/CLUSREG_CONDITION_IS_EQUAL","msclus/CLUSREG_CONDITION_IS_GREATER_THAN","msclus/CLUSREG_CONDITION_IS_KEY_NOT_EXISTS","msclus/CLUSREG_CONDITION_IS_LESS_THAN","msclus/CLUSREG_CONDITION_IS_NOT_EQUAL","msclus/CLUSREG_CONDITION_KEY_EXISTS","msclus/CLUSREG_CONDITION_NOT_EXISTS","msclus/CLUSREG_CONTROL_COMMAND","msclus/CLUSREG_CREATE_KEY","msclus/CLUSREG_DELETE_KEY","msclus/CLUSREG_DELETE_VALUE","msclus/CLUSREG_LAST_COMMAND","msclus/CLUSREG_READ_ERROR","msclus/CLUSREG_READ_VALUE","msclus/CLUSREG_SET_KEY_SECURITY","msclus/CLUSREG_SET_VALUE","msclus/CLUSREG_VALUE_DELETED","msclus/CLUSTER_REG_COMMAND","msclus/_CLUSTER_REG_COMMAND","mscs.cluster_reg_command"]
old-location: mscs\cluster_reg_command.htm
tech.root: MsCS
ms.assetid: 1a1266dc-a223-48bd-be30-80c8b50c5b21
ms.date: 12/05/2018
ms.keywords: CLUSREG_COMMAND_NONE, CLUSREG_CONDITION_EXISTS, CLUSREG_CONDITION_IS_EQUAL, CLUSREG_CONDITION_IS_GREATER_THAN, CLUSREG_CONDITION_IS_KEY_NOT_EXISTS, CLUSREG_CONDITION_IS_LESS_THAN, CLUSREG_CONDITION_IS_NOT_EQUAL, CLUSREG_CONDITION_KEY_EXISTS, CLUSREG_CONDITION_NOT_EXISTS, CLUSREG_CONTROL_COMMAND, CLUSREG_CREATE_KEY, CLUSREG_DELETE_KEY, CLUSREG_DELETE_VALUE, CLUSREG_LAST_COMMAND, CLUSREG_READ_ERROR, CLUSREG_READ_VALUE, CLUSREG_SET_KEY_SECURITY, CLUSREG_SET_VALUE, CLUSREG_VALUE_DELETED, CLUSTER_REG_COMMAND, CLUSTER_REG_COMMAND enumeration [Failover Cluster], _CLUSTER_REG_COMMAND, _CLUSTER_REG_COMMAND enumeration [Failover Cluster], clusapi/CLUSREG_COMMAND_NONE, clusapi/CLUSREG_CONDITION_EXISTS, clusapi/CLUSREG_CONDITION_IS_EQUAL, clusapi/CLUSREG_CONDITION_IS_GREATER_THAN, clusapi/CLUSREG_CONDITION_IS_KEY_NOT_EXISTS, clusapi/CLUSREG_CONDITION_IS_LESS_THAN, clusapi/CLUSREG_CONDITION_IS_NOT_EQUAL, clusapi/CLUSREG_CONDITION_KEY_EXISTS, clusapi/CLUSREG_CONDITION_NOT_EXISTS, clusapi/CLUSREG_CONTROL_COMMAND, clusapi/CLUSREG_CREATE_KEY, clusapi/CLUSREG_DELETE_KEY, clusapi/CLUSREG_DELETE_VALUE, clusapi/CLUSREG_LAST_COMMAND, clusapi/CLUSREG_READ_ERROR, clusapi/CLUSREG_READ_VALUE, clusapi/CLUSREG_SET_KEY_SECURITY, clusapi/CLUSREG_SET_VALUE, clusapi/CLUSREG_VALUE_DELETED, clusapi/CLUSTER_REG_COMMAND, clusapi/_CLUSTER_REG_COMMAND, msclus/CLUSREG_COMMAND_NONE, msclus/CLUSREG_CONDITION_EXISTS, msclus/CLUSREG_CONDITION_IS_EQUAL, msclus/CLUSREG_CONDITION_IS_GREATER_THAN, msclus/CLUSREG_CONDITION_IS_KEY_NOT_EXISTS, msclus/CLUSREG_CONDITION_IS_LESS_THAN, msclus/CLUSREG_CONDITION_IS_NOT_EQUAL, msclus/CLUSREG_CONDITION_KEY_EXISTS, msclus/CLUSREG_CONDITION_NOT_EXISTS, msclus/CLUSREG_CONTROL_COMMAND, msclus/CLUSREG_CREATE_KEY, msclus/CLUSREG_DELETE_KEY, msclus/CLUSREG_DELETE_VALUE, msclus/CLUSREG_LAST_COMMAND, msclus/CLUSREG_READ_ERROR, msclus/CLUSREG_READ_VALUE, msclus/CLUSREG_SET_KEY_SECURITY, msclus/CLUSREG_SET_VALUE, msclus/CLUSREG_VALUE_DELETED, msclus/CLUSTER_REG_COMMAND, msclus/_CLUSTER_REG_COMMAND, mscs.cluster_reg_command
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
req.typenames: CLUSTER_REG_COMMAND
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLUSTER_REG_COMMAND
 - clusapi/_CLUSTER_REG_COMMAND
 - CLUSTER_REG_COMMAND
 - clusapi/CLUSTER_REG_COMMAND
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
 - CLUSTER_REG_COMMAND
---

## -description

Enumerates the possible cluster registry commands that a local node will perform when attempting to join a cluster.  It is used by the <a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_batch_command">CLUSTER_BATCH_COMMAND</a> and <a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_read_batch_command">CLUSTER_READ_BATCH_COMMAND</a> structures.

## -enum-fields

### -field CLUSREG_COMMAND_NONE:0

This constant is not a valid command. It and the <b>CLUSREG_LAST_COMMAND</b> constant act as brackets  that contain the valid commands.

### -field CLUSREG_SET_VALUE:1

This command sets a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or (if not provided) relative to a key passed into  the <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatebatch">ClusterRegCreateBatch</a> function.

### -field CLUSREG_CREATE_KEY

This command will create a specified cluster registry key if it does not exist, or opens an existing one.

### -field CLUSREG_DELETE_KEY

This command will delete a key with all values and nested subkeys.  No commands that operate on values can follow <b>CLUSREG_DELETE_KEY</b> until <b>CLUSREG_CREATE_KEY</b> is added.

### -field CLUSREG_DELETE_VALUE

This command deletes a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or (if not provided) relative to a key passed into  the <a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatebatch">ClusterRegCreateBatch</a> function.

### -field CLUSREG_SET_KEY_SECURITY

This command is reserved for future use.

### -field CLUSREG_VALUE_DELETED

This command is returned only through a batch update notification port. It indicates whether a  specific cluster registry value has been deleted or whether the data of that cluster registry value has been changed.

### -field CLUSREG_READ_KEY

This command indicates that content was read successfully for the requested key.

### -field CLUSREG_READ_VALUE

This command indicates that content was read successfully for the requested value.

### -field CLUSREG_READ_ERROR

This command indicates that a value was missing or another error occurred during read.

### -field CLUSREG_CONTROL_COMMAND

A control command.

<b>Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2012 R2.

### -field CLUSREG_CONDITION_EXISTS

A condition that indicates that a value exists.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2016.

### -field CLUSREG_CONDITION_NOT_EXISTS

A condition that indicates that a value does not exist.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2016.

### -field CLUSREG_CONDITION_IS_EQUAL

A condition that indicates that a value is equal to another.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2016.

### -field CLUSREG_CONDITION_IS_NOT_EQUAL

A condition that indicates that a value is not equal to another.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2016.

### -field CLUSREG_CONDITION_IS_GREATER_THAN

A condition that indicates that a value is greater than another.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2016.

### -field CLUSREG_CONDITION_IS_LESS_THAN

A condition that indicates that a value is less than another.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2016.

### -field CLUSREG_CONDITION_KEY_EXISTS

A condition that indicates that a key exists.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2016.

### -field CLUSREG_CONDITION_KEY_NOT_EXISTS

A condition that indicates that a key does not exist.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2016.

### -field CLUSREG_LAST_COMMAND

This constant is not a valid command. It and the <b>CLUSREG_COMMAND_NONE</b> constant act as brackets  that contain the valid commands.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>The value of this constant is lower before Windows Server 2016.

## -remarks

The <b>CLUSREG_VALUE_DELETED</b> command precedes every <b>CLUSREG_SET_VALUE</b> and <b>CLUSREG_DELETE_VALUE</b> command in the returned notification data, if the value had existing data.

## -see-also

<a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_batch_command">CLUSTER_BATCH_COMMAND</a>

<a href="/windows/desktop/api/clusapi/ns-clusapi-cluster_read_batch_command">CLUSTER_READ_BATCH_COMMAND</a>

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatebatch">ClusterRegCreateBatch</a>

<a href="/previous-versions/windows/desktop/api/clusapi/nf-clusapi-clusterregcreatereadbatch">ClusterRegCreateReadBatch</a>

<a href="/previous-versions/windows/desktop/mscs/cluster-enumerations">Failover Cluster Enumerations</a>
