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

# DsReplicaSyncW function


## -description


The <b>DsReplicaSync</b> function synchronizes a destination naming context (NC) with one of its sources.


## -parameters




### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param NameContext [in]

Pointer to a constant null-terminated string that specifies the distinguished name of the destination NC.


### -param pUuidDsaSrc [in]

Pointer to the UUID of a source that replicates to the destination NC.


### -param Options [in]

Passes additional data used to process the request. This parameter can be a combination of the following values.



#### DS_REPSYNC_ADD_REFERENCE

Causes the source directory system agent (DSA) to verify that the local DSA is present in the source replicates-to list. If not, the local DSA is added. This ensures that the source sends change notifications.



#### DS_REPSYNC_ALL_SOURCES

This value is not supported.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Synchronizes from all sources.



#### DS_REPSYNC_ASYNCHRONOUS_OPERATION

Performs this operation asynchronously.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Required when using <b>DS_REPSYNC_ALL_SOURCES</b>.



#### DS_REPSYNC_FORCE

Synchronizes even if the link is currently disabled.



#### DS_REPSYNC_FULL

Synchronizes starting from the first Update Sequence Number (USN).



#### DS_REPSYNC_INTERSITE_MESSAGING

Synchronizes using an ISM.



#### DS_REPSYNC_NO_DISCARD

Does not discard this synchronization request, even if a similar synchronization is pending.



#### DS_REPSYNC_PERIODIC

Indicates this operation is a periodic synchronization request as scheduled by the administrator.



#### DS_REPSYNC_URGENT

Indicates this operation is a notification of an update marked urgent.



#### DS_REPSYNC_WRITEABLE

Replica is writable. Otherwise, it is read-only.


##### - Options.DS_REPSYNC_ADD_REFERENCE

Causes the source directory system agent (DSA) to verify that the local DSA is present in the source replicates-to list. If not, the local DSA is added. This ensures that the source sends change notifications.


##### - Options.DS_REPSYNC_ALL_SOURCES

This value is not supported.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Synchronizes from all sources.


##### - Options.DS_REPSYNC_ASYNCHRONOUS_OPERATION

Performs this operation asynchronously.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Required when using <b>DS_REPSYNC_ALL_SOURCES</b>.


##### - Options.DS_REPSYNC_FORCE

Synchronizes even if the link is currently disabled.


##### - Options.DS_REPSYNC_FULL

Synchronizes starting from the first Update Sequence Number (USN).


##### - Options.DS_REPSYNC_INTERSITE_MESSAGING

Synchronizes using an ISM.


##### - Options.DS_REPSYNC_NO_DISCARD

Does not discard this synchronization request, even if a similar synchronization is pending.


##### - Options.DS_REPSYNC_PERIODIC

Indicates this operation is a periodic synchronization request as scheduled by the administrator.


##### - Options.DS_REPSYNC_URGENT

Indicates this operation is a notification of an update marked urgent.


##### - Options.DS_REPSYNC_WRITEABLE

Replica is writable. Otherwise, it is read-only.


## -returns



If the function performs its operation successfully, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the standard Win32 API errors.




## -remarks



The server that <b>DsReplicaSync</b> executes on is called the destination. The destination naming context is brought up-to-date with respect to a source system, identified by the UUID of the source system NTDS Settings object. The destination system must already be configured so that the source system is one of the systems from which it receives replication data.

<div class="alert"><b>Note</b>  Forcing manual synchronization can prevent the directory service from properly prioritizing replication operations. For example, synchronizing a new user may preempt an urgent synchronization performed to provide access to a recently locked out user or to add a new trust password. If you call this API often, you can flood the network with requests, which can interfere with other replication operations. For this reason, it is strongly recommended that this function be used only for single-use scenarios rather than incorporating it into an application that would use it on a regular basis.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/33bd1b61-b9ed-479f-a128-fb7ddbb5e9af">DsReplicaAdd</a>



<a href="https://msdn.microsoft.com/68c767c4-bbb6-477b-8ffb-94f3ae235375">DsReplicaDel</a>



<a href="https://msdn.microsoft.com/aad20527-1211-41bc-b0e9-02e4ab28ae2e">DsReplicaModify</a>



<a href="https://msdn.microsoft.com/158c7e73-0e6c-4b71-a87f-2f60f3db91cb">DsReplicaUpdateRefs</a>
 

 

