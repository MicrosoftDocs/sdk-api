---
UID: NF:clusapi.ClusterRegBatchReadCommand
title: ClusterRegBatchReadCommand function
author: windows-sdk-content
description: Reads a command from a batch notification.
old-location: mscs\clusterregbatchreadcommand.htm
old-project: mscs
ms.assetid: a1a7abc5-f306-4664-bb53-e54c6ee1051e
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusterRegBatchReadCommand, ClusterRegBatchReadCommand function [Failover Cluster], PCLUSTER_REG_GET_BATCH_NOTIFICATION, clusapi/ClusterRegBatchReadCommand, mscs.clusterregbatchreadcommand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: SR_REPLICATED_DISK_TYPE, *PSR_REPLICATED_DISK_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ClusAPI.dll
api_name:
 - ClusterRegBatchReadCommand
product: Windows
targetos: Windows
req.lib: ClusAPI.lib
req.dll: ClusAPI.dll
req.irql: 
---

# ClusterRegBatchReadCommand function


## -description


Reads a command from a batch notification.


## -parameters




### -param hBatchNotification [in]

A handle to the batch notification.


### -param pBatchCommand [out]

Pointer to a <a href="https://msdn.microsoft.com/31f8e255-80c8-4381-a8f3-0d48a3831a89">CLUSTER_BATCH_COMMAND</a> structure 
       that will be filled with information about the command on successful return.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



The <b>PCLUSTER_REG_GET_BATCH_NOTIFICATION</b> type defines a pointer to this 
     function.




## -see-also




<a href="https://msdn.microsoft.com/31f8e255-80c8-4381-a8f3-0d48a3831a89">CLUSTER_BATCH_COMMAND</a>



<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>
 

 

