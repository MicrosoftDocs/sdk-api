---
UID: NF:clusapi.ClusterRegBatchCloseNotification
title: ClusterRegBatchCloseNotification function
author: windows-sdk-content
description: Frees the memory associated with the batch notification.
old-location: mscs\clusterregbatchclosenotification.htm
tech.root: mscs
ms.assetid: d7a127ba-6e97-46ac-8510-2da355359c50
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: ClusterRegBatchCloseNotification, ClusterRegBatchCloseNotification function [Failover Cluster], PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION, clusapi/ClusterRegBatchCloseNotification, mscs.clusterregbatchclosenotification
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
 - ClusterRegBatchCloseNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ClusterRegBatchCloseNotification function


## -description


Frees the memory associated with the batch notification.


## -parameters




### -param hBatchNotification [in]

A handle to the batch notification.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/en-us/library/ms681381(v=VS.85).aspx">system error codes</a>.




## -remarks



The <b>PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION</b> type defines a pointer to this 
     function.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa369128(v=VS.85).aspx">Cluster Registry Access Functions</a>
 

 

