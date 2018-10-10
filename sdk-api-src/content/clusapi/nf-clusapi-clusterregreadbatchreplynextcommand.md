---
UID: NF:clusapi.ClusterRegReadBatchReplyNextCommand
title: ClusterRegReadBatchReplyNextCommand function
author: windows-sdk-content
description: Reads the next command from a read batch result.
old-location: mscs\clusterregreadbatchreplynextcommand.htm
tech.root: MsCS
ms.assetid: 4E0DEB5C-36AA-480C-913C-235DE9AEA58D
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ClusterRegReadBatchReplyNextCommand, ClusterRegReadBatchReplyNextCommand function [Failover Cluster], clusapi/ClusterRegReadBatchReplyNextCommand, mscs.clusterregreadbatchreplynextcommand
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-0.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegReadBatchReplyNextCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegReadBatchReplyNextCommand function


## -description


Reads the next command from a read batch result.


## -parameters




### -param hRegReadBatchReply [in]

A handle to a read batch result that was created by calling the <a href="https://msdn.microsoft.com/A164EB9F-290E-446E-98E9-95C6C3C3D00C">ClusterRegCloseReadBatch</a> function.  You must close this handle later by calling the  <a href="https://msdn.microsoft.com/en-us/library/Hh706742(v=VS.85).aspx">ClusterRegCloseReadBatchReply</a> function.


### -param pBatchCommand [out]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Hh706767(v=VS.85).aspx">CLUSTER_READ_BATCH_COMMAND</a> structure that contains information about the read command.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



The number of records in the read batch results is equal to the number of commands in the read batch. Also, the results are in the same order as the commands that were added to the read batch.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh706767(v=VS.85).aspx">CLUSTER_READ_BATCH_COMMAND</a>



<a href="https://msdn.microsoft.com/A164EB9F-290E-446E-98E9-95C6C3C3D00C">ClusterRegCloseReadBatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh706742(v=VS.85).aspx">ClusterRegCloseReadBatchReply</a>
 

 

