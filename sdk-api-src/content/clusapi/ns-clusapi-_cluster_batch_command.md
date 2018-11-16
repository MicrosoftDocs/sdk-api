---
UID: NS:clusapi._CLUSTER_BATCH_COMMAND
title: "_CLUSTER_BATCH_COMMAND"
author: windows-sdk-content
description: Represents the order in which current batch command data is sent to the ClusterRegBatchReadCommand function.
old-location: mscs\cluster_batch_command.htm
tech.root: MsCS
ms.assetid: 31f8e255-80c8-4381-a8f3-0d48a3831a89
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CLUSREG_CREATE_KEY, CLUSREG_DELETE_KEY, CLUSREG_DELETE_VALUE, CLUSREG_SET_VALUE, CLUSREG_VALUE_DELETED, CLUSTER_BATCH_COMMAND, CLUSTER_BATCH_COMMAND structure [Failover Cluster], _CLUSTER_BATCH_COMMAND, clusapi/CLUSTER_BATCH_COMMAND, mscs.cluster_batch_command
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ClusAPI.h
api_name:
 - CLUSTER_BATCH_COMMAND
product: Windows
targetos: Windows
req.typenames: CLUSTER_BATCH_COMMAND
req.redist: 
---

# _CLUSTER_BATCH_COMMAND structure


## -description


Represents the order in which current batch command data is sent to the 
    <a href="https://msdn.microsoft.com/a1a7abc5-f306-4664-bb53-e54c6ee1051e">ClusterRegBatchReadCommand</a> 
    function. Values in the 
    <b>CLUSTER_BATCH_COMMAND</b> structure are identical to 
    parameters passed to the 
    <a href="https://msdn.microsoft.com/3d59e68a-deb3-443f-9d8f-281cdb15e8b6">ClusterRegBatchAddCommand</a> function. The only 
    difference is that for <b>CLUSREG_DELETE_VALUE</b>, the <b>dwOptions</b>, 
    <b>lpData</b>, and <b>cbData</b> members are set to the value being 
    deleted, similar to the <b>CLUSREG_SET_VALUE</b> command.


## -struct-fields




### -field Command

A command that is supported by this API and taken from the 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309163(v=VS.85).aspx">CLUSTER_REG_COMMAND</a> enumeration. The possible 
       commands are as follows.



#### CLUSREG_SET_VALUE (1)

Sets a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or (if not 
         provided) relative to a key passed into the 
         <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a> function.



#### CLUSREG_CREATE_KEY (2)

Creates a specified cluster registry key if it does not exist, or opens an existing one.



#### CLUSREG_DELETE_KEY (3)

Deletes a key with all values and nested subkeys.  No commands that operate on values can follow 
         <b>CLUSREG_DELETE_KEY</b> until <b>CLUS_REG_CREATE_KEY</b> is 
         added.



#### CLUSREG_DELETE_VALUE (4)

Deletes a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or (if 
         not provided) relative to a key passed into the 
         <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a> function.



#### CLUSREG_VALUE_DELETED (6)

Indicates whether a  specific cluster registry value has been deleted or if the data of that cluster 
         registry value has been changed. This command is returned only through a batch update notification port.


### -field dwOptions

If the <b>Command</b> member takes either the 
       <b>CLUSREG_SET_VALUE</b> command or the <b>CLUSREG_DELETE_VALUE</b> 
       command, then this member takes one of the standard 
       <a href="https://msdn.microsoft.com/en-us/library/ms724884(v=VS.85).aspx">registry value types</a>. If not, then 
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
     <a href="https://msdn.microsoft.com/d7a127ba-6e97-46ac-8510-2da355359c50">ClusterRegBatchCloseNotification</a> 
     function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309163(v=VS.85).aspx">CLUSTER_REG_COMMAND</a>



<a href="https://msdn.microsoft.com/3d59e68a-deb3-443f-9d8f-281cdb15e8b6">ClusterRegBatchAddCommand</a>



<a href="https://msdn.microsoft.com/d7a127ba-6e97-46ac-8510-2da355359c50">ClusterRegBatchCloseNotification</a>



<a href="https://msdn.microsoft.com/a1a7abc5-f306-4664-bb53-e54c6ee1051e">ClusterRegBatchReadCommand</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369165(v=VS.85).aspx">Failover Cluster Structures</a>
 

 

