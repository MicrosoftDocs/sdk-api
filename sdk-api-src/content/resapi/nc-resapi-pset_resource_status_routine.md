---
UID: NC:resapi.PSET_RESOURCE_STATUS_ROUTINE
title: PSET_RESOURCE_STATUS_ROUTINE
author: windows-sdk-content
description: Called to update the status of a resource.
old-location: mscs\setresourcestatus.htm
tech.root: mscs
ms.assetid: 8ddb4578-f8c4-462e-af04-8c537d585e8b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSET_RESOURCE_STATUS_ROUTINE, PSET_RESOURCE_STATUS_ROUTINE callback function [Failover Cluster], SetResourceStatus, SetResourceStatus callback, SetResourceStatus callback function [Failover Cluster], _wolf_setresourcestatus, mscs.setresourcestatus, resapi/PSET_RESOURCE_STATUS_ROUTINE, resapi/SetResourceStatus
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - SetResourceStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSET_RESOURCE_STATUS_ROUTINE callback function


## -description


Called to update the status of a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. 
    The <b>PSET_RESOURCE_STATUS_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param ResourceHandle [in]

Handle identifying the resource to be updated. The <i>ResourceHandle</i> parameter should 
       contain the same handle used for the <i>ResourceHandle</i> parameter in the 
       <a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a> entry point for this resource.


### -param ResourceStatus [in]

Pointer to a <a href="https://msdn.microsoft.com/a5acd51f-714f-481b-85e2-ac82b76d21bb">RESOURCE_STATUS</a> structure that 
       contains information about the resource's state.


## -returns



<i>SetResourceStatus</i> returns one of 
       the following values enumerated from the 
       <a href="https://msdn.microsoft.com/d1b9fd8f-7d49-4396-8f0c-6db8fad5749e">RESOURCE_EXIT_STATE</a> enumeration.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ResourceExitStateContinue</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The resource has not been terminated. Worker threads may continue 
         <a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a> and 
         <a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a> operations for the resource.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ResourceExitStateTerminate</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The resource has been terminated. Callers should end 
         <a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a> or 
         <a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a> operations and immediately terminate all worker 
         threads assigned to the resource.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">Resource DLLs</a> call the 
     <i>SetResourceStatus</i> callback function to update the 
     status of a resource after their <a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a> or 
     <a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a> entry point function has returned 
     <b>ERROR_IO_PENDING</b>. It should not be called at any other time. A pointer to the 
     <i>SetResourceStatus</i> function is passed in the 
     <i>SetResourceStatus</i> parameter to the resource's implementation of 
     <a href="https://msdn.microsoft.com/b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3">Startup</a>.

<i>SetResourceStatus</i> is implemented by the 
     <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> and is similar to the 
     <a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a> function.

Update the current state of a resource whenever necessary after you have returned 
     <b>ERROR_IO_PENDING</b>. If the resource is in one of the pending states, increment the values 
     for the <b>CheckPoint</b> and <b>WaitHint</b> members of the 
     <a href="https://msdn.microsoft.com/a5acd51f-714f-481b-85e2-ac82b76d21bb">RESOURCE_STATUS</a> structure and set the 
     <b>ResourceState</b> member to <b>ClusterResourceOnlinePending</b> or 
     <b>ClusterResourceOfflinePending</b> before you begin calling 
     <i>SetResourceStatus</i>. Call 
     <i>SetResourceStatus</i> until one of the following 
     situations occurs:

<ul>
<li>The resource is placed in either the <b>ClusterResourceOnline</b> or 
      <b>ClusterResourceOffline</b> state.</li>
<li>The time limit stored in the resource's 
      <a href="https://msdn.microsoft.com/12f5cb51-7c7c-49b1-8542-dbbff50d55b0">PendingTimeout</a> property has been 
      exceeded.</li>
</ul>
There is no need to call 
     <i>SetResourceStatus</i> to set the state of a resource to 
     a pending state because the Resource Monitor automatically sets it to the appropriate pending state whenever 
     <a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a> or 
     <a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a> returns 
     <b>ERROR_IO_PENDING</b>.




## -see-also




<a href="https://msdn.microsoft.com/d143a860-92fe-4fa9-b0d7-d591376a0209">ClusWorkerTerminate</a>



<a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a>



<a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a>



<a href="https://msdn.microsoft.com/0a5c10c5-0380-4638-b49d-396be3b3c0dd">Open</a>



<a href="https://msdn.microsoft.com/d1b9fd8f-7d49-4396-8f0c-6db8fad5749e">RESOURCE_EXIT_STATE</a>



<a href="https://msdn.microsoft.com/a5acd51f-714f-481b-85e2-ac82b76d21bb">RESOURCE_STATUS</a>



<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>



<a href="https://msdn.microsoft.com/bb5943ff-2814-40f2-bee0-ae7132befde9">SetServiceStatus</a>



<a href="https://msdn.microsoft.com/b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3">Startup</a>



<a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>
 

 

