---
UID: NF:ntdsapi.DsReplicaConsistencyCheck
title: DsReplicaConsistencyCheck function
author: windows-driver-content
description: Invokes the Knowledge Consistency Checker (KCC) to verify the replication topology.
old-location: ad\dsreplicaconsistencycheck.htm
old-project: AD
ms.assetid: 2a83ffcb-1ebd-4024-a186-9c079896f4e1
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: DS_KCC_FLAG_ASYNC_OP, DS_KCC_FLAG_DAMPED, DsReplicaConsistencyCheck, DsReplicaConsistencyCheck function [Active Directory], _glines_dsreplicaconsistencycheck, ad.dsreplicaconsistencycheck, ntdsapi/DsReplicaConsistencyCheck
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DS_REPL_OP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdsapi.dll
api_name:
-	DsReplicaConsistencyCheck
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
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
 

 

