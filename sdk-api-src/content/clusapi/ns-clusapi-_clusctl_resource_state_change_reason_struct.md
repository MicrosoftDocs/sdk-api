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

# _CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT structure


## -description


Sent with the 
    <a href="https://msdn.microsoft.com/3261c8eb-b88b-428a-8a2b-684e0967f9de">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a> 
    control code to provide the reason for a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> state 
    change.


## -struct-fields




### -field dwSize

The size of the structure in bytes.


### -field dwVersion

The version of the structure. Set to 
       <b>CLUSCTL_RESOURCE_STATE_CHANGE_REASON_VERSION_1</b> (1).


### -field eReason

A value of the 
      <a href="https://msdn.microsoft.com/f9071688-24c2-4b00-ac66-6cf0363bccf2">CLUSTER_RESOURCE_STATE_CHANGE_REASON</a> 
      enumeration that describes the reason for the state change. The following list lists the possible values.



#### eResourceStateChangeReasonUnknown (0)

This reason code is never sent by the cluster. 
         <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">Resource DLLs</a> should use this value to initialize a 
         local 
         <b>CLUSCTL_RESOURCE_STATE_CHANGE_REASON_STRUCT</b> 
         structure and to reset the <b>eReason</b> member of this structure before returning from 
         the <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a> 
         and <a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a> entry point functions. For more 
         information, see 
         <a href="https://msdn.microsoft.com/3261c8eb-b88b-428a-8a2b-684e0967f9de">CLUSCTL_RESOURCE_STATE_CHANGE_REASON</a>.



#### eResourceStateChangeReasonMove (1)


<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a> is about to be called because the 
         <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource's</a> <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> is being moved.



#### eResourceStateChangeReasonFailover (2)


<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a> is about to be called because the 
         resource's group is being <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">failed over</a>.



#### eResourceStateChangeReasonFailedMove (3)


<a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a> is about to be called because the resource's 
         group did not successfully complete a move operation.



#### eResourceStateChangeReasonShutdown (4)


<a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a> is about to be called because the 
         <a href="https://msdn.microsoft.com/90717d6e-f2a4-49a0-86b6-17de1c4bcfe4">Cluster service</a> is being shut down.



#### eResourceStateChangeReasonRundown (5)


<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a> is about to be called because the Cluster 
         service has stopped unexpectedly.


## -see-also




<a href="https://msdn.microsoft.com/f9071688-24c2-4b00-ac66-6cf0363bccf2">CLUSTER_RESOURCE_STATE_CHANGE_REASON</a>



<a href="https://msdn.microsoft.com/45da8dbc-dd70-4f95-b933-66d8e4340448">Utility Structures</a>
 

 

