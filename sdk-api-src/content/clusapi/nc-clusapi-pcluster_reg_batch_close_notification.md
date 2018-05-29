---
UID: NC:clusapi.PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION
title: PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION
author: windows-sdk-content
description: Frees the memory associated with the batch notification.
old-location: mscs\clusterregbatchclosenotification.htm
old-project: MsCS
ms.assetid: d7a127ba-6e97-46ac-8510-2da355359c50
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION, PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION callback, PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION callback function [Failover Cluster], clusapi/PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION, mscs.clusterregbatchclosenotification
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
req.typenames: Sources
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ClusAPI.h
api_name:
-	PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION callback function


## -description


Frees the memory associated with the batch notification.


## -parameters




### -param hBatchNotification [in]

A handle to the batch notification.


## -returns



The function returns one of the following 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



The <b>PCLUSTER_REG_BATCH_CLOSE_NOTIFICATION</b> type defines a pointer to this 
     function.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>
 

 

