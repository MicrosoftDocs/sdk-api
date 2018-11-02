---
UID: NF:clusapi.ClusterRegBatchReadCommand
title: ClusterRegBatchReadCommand function
author: windows-sdk-content
description: Reads a command from a batch notification.
old-location: mscs\clusterregbatchreadcommand.htm
tech.root: mscs
ms.assetid: a1a7abc5-f306-4664-bb53-e54c6ee1051e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ClusterRegBatchReadCommand, ClusterRegBatchReadCommand function [Failover Cluster], PCLUSTER_REG_GET_BATCH_NOTIFICATION, clusapi/ClusterRegBatchReadCommand, mscs.clusterregbatchreadcommand
ms.prod: windows-hardware
ms.technology: windows-devices
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
api_name:
 - ClusterRegBatchReadCommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegBatchReadCommand function


## -description


Reads a command from a batch notification.


## -parameters




### -param hBatchNotification [in]

A handle to the batch notification.


### -param pBatchCommand [out]

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/Cc512181(v=VS.85).aspx">CLUSTER_BATCH_COMMAND</a> structure 
       that will be filled with information about the command on successful return.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



The <b>PCLUSTER_REG_GET_BATCH_NOTIFICATION</b> type defines a pointer to this 
     function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Cc512181(v=VS.85).aspx">CLUSTER_BATCH_COMMAND</a>



<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>
 

 

