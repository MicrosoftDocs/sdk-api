---
UID: NF:clusapi.ClusterRegCloseBatchEx
title: ClusterRegCloseBatchEx function
author: windows-sdk-content
description: Executes or ignores the batch created by the ClusterRegCreateBatch function.
old-location: mscs\clusterregclosebatchex.htm
tech.root: mscs
ms.assetid: 127d06de-28a4-4df4-9f5f-17ea4a330528
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ClusterRegCloseBatchEx, ClusterRegCloseBatchEx function [Failover Cluster], clusapi/ClusterRegCloseBatchEx, mscs.clusterregclosebatchex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 R2
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
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-1.dll
 - Ext-MS-Win-Cluster-ClusAPI-l1-1-2.dll
api_name:
 - ClusterRegCloseBatchEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegCloseBatchEx function


## -description


Executes or ignores the batch created by the 
    <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a> function.


## -parameters




### -param hRegBatch [in]

The handle of the  cluster registry key opened by 
       <a href="https://msdn.microsoft.com/en-us/library/Bb309132(v=VS.85).aspx">ClusterRegCreateBatch</a>. After the completion 
       of <a href="https://msdn.microsoft.com/d43644cf-370b-499f-b321-24e43f145a98">ClusterRegCloseBatch</a>, this handle is no 
       longer valid and memory associated with it is freed.


### -param flags [in]


### -param failedCommandNumber [out, optional]

If execution of the batch is not successful, the number of the command that failed is returned in the form of 
       a <i>failedCommandNumber</i> argument. The first command in the batch has number 0, the 
       second has number 1, and so on.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



If a failure has occurred before any command was executed, the <i>failedCommandNumber</i> 
     parameter is set to –1.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369128(v=VS.85).aspx">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/d43644cf-370b-499f-b321-24e43f145a98">ClusterRegCloseBatch</a>
 

 

