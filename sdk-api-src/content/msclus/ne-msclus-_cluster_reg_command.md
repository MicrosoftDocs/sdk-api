---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _CLUSTER_REG_COMMAND enumeration


## -description


Enumerates the possible cluster registry commands that a local node will perform when attempting to join a cluster.  It is used by the <a href="https://msdn.microsoft.com/31f8e255-80c8-4381-a8f3-0d48a3831a89">CLUSTER_BATCH_COMMAND</a> and <a href="https://msdn.microsoft.com/BE7D4B99-27C0-4CAA-BFDC-669737E17D86">CLUSTER_READ_BATCH_COMMAND</a> structures.


## -enum-fields




### -field CLUSREG_COMMAND_NONE

This constant is not a valid command. It and the <b>CLUSREG_LAST_COMMAND</b> constant act as brackets  that contain the valid commands.


### -field CLUSREG_SET_VALUE

This command sets a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or (if not provided) relative to a key passed into  the <a href="https://msdn.microsoft.com/83e7c216-f08f-4dc2-9b53-faa2760985d4">ClusterRegCreateBatch</a> function.


### -field CLUSREG_CREATE_KEY

This command will create a specified cluster registry key if it does not exist, or opens an existing one.


### -field CLUSREG_DELETE_KEY

This command will delete a key with all values and nested subkeys.  No commands that operate on values can follow <b>CLUSREG_DELETE_KEY</b> until <b>CLUSREG_CREATE_KEY</b> is added.


### -field CLUSREG_DELETE_VALUE

This command deletes a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or (if not provided) relative to a key passed into  the <a href="https://msdn.microsoft.com/83e7c216-f08f-4dc2-9b53-faa2760985d4">ClusterRegCreateBatch</a> function.


### -field CLUSREG_SET_KEY_SECURITY

This command is reserved for future use.


### -field CLUSREG_VALUE_DELETED

This command is returned only through a batch update notification port. It indicates whether a  specific cluster registry value has been deleted or whether the data of that cluster registry value has been changed.


### -field CLUSREG_READ_KEY


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


### -field CLUSREG_LAST_COMMAND

This constant is not a valid command. It and the <b>CLUSREG_COMMAND_NONE</b> constant act as brackets  that contain the valid commands.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>The value of this constant is lower before Windows Server 2016.


#### - CLUSREG_CONDITION_IS_KEY_NOT_EXISTS

A condition that indicates that a key does not exist.

<b>Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  </b>This value is not available before Windows Server 2016.


## -remarks



The <b>CLUSREG_VALUE_DELETED</b> command precedes every <b>CLUSREG_SET_VALUE</b> and <b>CLUSREG_DELETE_VALUE</b> command in the returned notification data, if the value had existing data.




## -see-also




<a href="https://msdn.microsoft.com/31f8e255-80c8-4381-a8f3-0d48a3831a89">CLUSTER_BATCH_COMMAND</a>



<a href="https://msdn.microsoft.com/BE7D4B99-27C0-4CAA-BFDC-669737E17D86">CLUSTER_READ_BATCH_COMMAND</a>



<a href="https://msdn.microsoft.com/83e7c216-f08f-4dc2-9b53-faa2760985d4">ClusterRegCreateBatch</a>



<a href="https://msdn.microsoft.com/FED3986E-7383-46C4-B2D5-259812EF63A2">ClusterRegCreateReadBatch</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

