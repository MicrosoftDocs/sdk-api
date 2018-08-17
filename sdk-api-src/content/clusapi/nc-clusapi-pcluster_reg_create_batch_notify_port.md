---
UID: NC:clusapi.PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT
title: PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT
author: windows-sdk-content
description: Creates a subscription to a batch notification port.
old-location: mscs\clusterregcreatebatchnotifyport.htm
old-project: mscs
ms.assetid: 1eca2ba5-c0c3-4388-9384-db9dbcfc8405
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT, PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT callback, PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT callback function [Failover Cluster], clusapi/PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT, mscs.clusterregcreatebatchnotifyport
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
 - PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT callback function


## -description


Creates a subscription to a batch notification port. The batch notification port needs to 
    be closed after it is no longer needed. This is done via the 
    <a href="https://msdn.microsoft.com/7ae10343-c97e-4036-9fe6-b894394bb605">ClusterRegCloseBatchNotifyPort</a> 
    function.


## -parameters




### -param hKey [in]

A cluster registry key. Any updates performed at this key or keys below it will be posted to a notification 
       port.


### -param *phBatchNotifyPort [out]

A handle to a batch notification port that allows subsequent reading batch notifications via the 
       <a href="https://msdn.microsoft.com/en-us/library/Cc512176(v=VS.85).aspx">ClusterRegGetBatchNotification</a> 
       function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error code</a>.




## -remarks



The <b>PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT</b> type defines a pointer to this 
     function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369128(v=VS.85).aspx">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/7ae10343-c97e-4036-9fe6-b894394bb605">ClusterRegCloseBatchNotifyPort</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc512176(v=VS.85).aspx">ClusterRegGetBatchNotification</a>
 

 

