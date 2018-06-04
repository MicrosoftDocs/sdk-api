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

# DsReplicaConsistencyCheck function


## -description


The <b>DsReplicaConsistencyCheck</b> function invokes the Knowledge Consistency Checker (KCC)  to verify the replication topology. The KCC dynamically adjusts the data replication topology of your network when domain controllers are added to or removed from the network, when a domain controller is unavailable, or when the data replication schedules are changed.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a>, 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a>, or <a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a> function.


### -param TaskID [in]

Identifies the task that the KCC should execute. <b>DS_KCC_TASKID_UPDATE_TOPOLOGY</b> is the only currently supported value.


### -param dwFlags [in]

Contains a set of flags that modify the function behavior. This can be zero or a combination of one or more of the following values.



#### DS_KCC_FLAG_ASYNC_OP

The task is queued and then the function returns without waiting for the task to complete.



#### DS_KCC_FLAG_DAMPED

The task will not be added to the queue if another queued task will run soon.


## -returns



If the function performs its operation successfully, the return value is <b>ERROR_SUCCESS</b>. If the function fails, the return value can be one of the following.




## -see-also




<a href="https://msdn.microsoft.com/61A2BB61-E3AE-4530-96CA-E7F85CB82DB2">DS_KCC_TASKID</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/9a149654-fd94-4b0c-b712-07fb827bef2f">DsBindWithSpn</a>
 

 

