---
UID: NC:clusapi.PCLUSTER_REG_BATCH_ADD_COMMAND
title: PCLUSTER_REG_BATCH_ADD_COMMAND
author: windows-sdk-content
description: Adds a command to a batch that will be executed on a cluster registry key.
old-location: mscs\clusterregbatchaddcommand.htm
old-project: mscs
ms.assetid: 3d59e68a-deb3-443f-9d8f-281cdb15e8b6
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CLUSREG_CREATE_KEY, CLUSREG_DELETE_KEY, CLUSREG_DELETE_VALUE, CLUSREG_SET_VALUE, PCLUSTER_REG_BATCH_ADD_COMMAND, PCLUSTER_REG_BATCH_ADD_COMMAND callback, PCLUSTER_REG_BATCH_ADD_COMMAND callback function [Failover Cluster], clusapi/PCLUSTER_REG_BATCH_ADD_COMMAND, mscs.clusterregbatchaddcommand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: Sources
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ClusAPI.h
api_name:
 - PCLUSTER_REG_BATCH_ADD_COMMAND
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSTER_REG_BATCH_ADD_COMMAND callback function


## -description


Adds a command to a batch that will be executed on a cluster registry key. Additional calls 
    to the function will yield additional commands added to the batch. The batch was created by the 
    <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a> function and will be 
    either executed or ignored by the 
    <a href="https://msdn.microsoft.com/d43644cf-370b-499f-b321-24e43f145a98">ClusterRegCloseBatch</a> function.


## -parameters




### -param hRegBatch [in]

The handle of the batch to which a command will be added.


### -param dwCommand [in]

A command supported by this API that is taken from the 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309163(v=VS.85).aspx">CLUSTER_REG_COMMAND</a> enumeration.  The possible 
       commands are as follows.



#### CLUSREG_SET_VALUE (1)

Sets a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or (if 
         not provided) relative to a key passed into the 
         <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a> function.



#### CLUSREG_CREATE_KEY (2)

Creates a specified cluster registry key if it does not exist, or opens an existing one.



#### CLUSREG_DELETE_KEY (3)

Deletes a key with all values and nested subkeys.  No commands that operate on values can follow 
         <b>CLUSREG_DELETE_KEY</b> until <b>CLUSREG_CREATE_KEY</b> is 
         added.



#### CLUSREG_DELETE_VALUE (4)

Deletes a value relative to the last executed <b>CLUSREG_CREATE_KEY</b> command or 
         (if not provided) relative to a key passed into  the 
         <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a> function.


### -param wzName [in, optional]

The name of the value or key relative to the command issued by the <i>dwCommand</i> 
       parameter.


### -param dwOptions [in]

If <i>dwCommand</i> takes the <b>CLUSREG_SET_VALUE</b> command, then 
       this parameter takes one of the standard 
       <a href="https://msdn.microsoft.com/en-us/library/ms724884(v=VS.85).aspx">registry value types</a>. If not, then 
       <i>dwCommand</i> is set to 0.


### -param *lpData [in, optional]

A pointer to the data relative to the command issued by <i>dwCommand</i>. The value of 
       this parameter is <b>NULL</b> for all but the <b>CLUSREG_SET_VALUE</b> 
       command.


### -param cbData [in]

The count, in bytes, of the data relative to the command issued by <i>dwCommand</i>. The 
       value of this parameter is 0 for all but the <b>CLUSREG_SET_VALUE</b> command.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



The <b>PCLUSTER_REG_BATCH_ADD_COMMAND</b> type defines a pointer to this function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb309163(v=VS.85).aspx">CLUSTER_REG_COMMAND</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa369128(v=VS.85).aspx">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/d43644cf-370b-499f-b321-24e43f145a98">ClusterRegCloseBatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a>



<a href="https://msdn.microsoft.com/en-us/library/ms724884(v=VS.85).aspx">Registry Value Types</a>
 

 

