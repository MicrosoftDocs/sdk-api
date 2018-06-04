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
       <a href="https://msdn.microsoft.com/4cc6925f-cf91-449b-8f9d-fcf48b4df896">ClusterRegGetBatchNotification</a> 
       function.


## -returns



If the operation succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>.




## -remarks



The <b>PCLUSTER_REG_CREATE_BATCH_NOTIFY_PORT</b> type defines a pointer to this 
     function.




## -see-also




<a href="https://msdn.microsoft.com/2bb0650f-ef9c-40bb-ae90-229bfa23838e">Cluster Registry Access Functions</a>



<a href="https://msdn.microsoft.com/7ae10343-c97e-4036-9fe6-b894394bb605">ClusterRegCloseBatchNotifyPort</a>



<a href="https://msdn.microsoft.com/4cc6925f-cf91-449b-8f9d-fcf48b4df896">ClusterRegGetBatchNotification</a>
 

 

