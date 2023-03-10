---
UID: NC:resapi.PSET_RESOURCE_STATUS_ROUTINE
title: PSET_RESOURCE_STATUS_ROUTINE (resapi.h)
description: The PSET_RESOURCE_STATUS_ROUTINE callback function is called to update the status of a resource.
helpviewer_keywords: ["PSET_RESOURCE_STATUS_ROUTINE","PSET_RESOURCE_STATUS_ROUTINE callback function [Failover Cluster]","SetResourceStatus","SetResourceStatus callback","SetResourceStatus callback function [Failover Cluster]","_wolf_setresourcestatus","mscs.setresourcestatus","resapi/PSET_RESOURCE_STATUS_ROUTINE","resapi/SetResourceStatus"]
old-location: mscs\setresourcestatus.htm
tech.root: MsCS
ms.assetid: 8ddb4578-f8c4-462e-af04-8c537d585e8b
ms.date: 08/03/2022
ms.keywords: PSET_RESOURCE_STATUS_ROUTINE, PSET_RESOURCE_STATUS_ROUTINE callback function [Failover Cluster], SetResourceStatus, SetResourceStatus callback, SetResourceStatus callback function [Failover Cluster], _wolf_setresourcestatus, mscs.setresourcestatus, resapi/PSET_RESOURCE_STATUS_ROUTINE, resapi/SetResourceStatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSET_RESOURCE_STATUS_ROUTINE
 - resapi/PSET_RESOURCE_STATUS_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - SetResourceStatus
---

# PSET_RESOURCE_STATUS_ROUTINE callback function


## -description

Called to update the status of a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. 
    The <b>PSET_RESOURCE_STATUS_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param ResourceHandle [in]

Handle identifying the resource to be updated. The <i>ResourceHandle</i> parameter should 
       contain the same handle used for the <i>ResourceHandle</i> parameter in the 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> entry point for this resource.

### -param ResourceStatus [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resource_status">RESOURCE_STATUS</a> structure that 
       contains information about the resource's state.

## -returns

<i>SetResourceStatus</i> returns one of 
       the following values enumerated from the 
       <a href="/windows/desktop/api/resapi/ne-resapi-resource_exit_state">RESOURCE_EXIT_STATE</a> enumeration.

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
         <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> and 
         <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> operations for the resource.

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
         <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> or 
         <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> operations and immediately terminate all worker 
         threads assigned to the resource.

</td>
</tr>
</table>

## -remarks

<a href="/previous-versions/windows/desktop/mscs/resource-dlls">Resource DLLs</a> call the 
     <i>SetResourceStatus</i> callback function to update the 
     status of a resource after their <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> or 
     <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> entry point function has returned 
     <b>ERROR_IO_PENDING</b>. It should not be called at any other time. A pointer to the 
     <i>SetResourceStatus</i> function is passed in the 
     <i>SetResourceStatus</i> parameter to the resource's implementation of 
     <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a>.

<i>SetResourceStatus</i> is implemented by the 
     <a href="/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a> and is similar to the 
     <a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> function.

Update the current state of a resource whenever necessary after you have returned 
     <b>ERROR_IO_PENDING</b>. If the resource is in one of the pending states, increment the values 
     for the <b>CheckPoint</b> and <b>WaitHint</b> members of the 
     <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resource_status">RESOURCE_STATUS</a> structure and set the 
     <b>ResourceState</b> member to <b>ClusterResourceOnlinePending</b> or 
     <b>ClusterResourceOfflinePending</b> before you begin calling 
     <i>SetResourceStatus</i>. Call 
     <i>SetResourceStatus</i> until one of the following 
     situations occurs:

<ul>
<li>The resource is placed in either the <b>ClusterResourceOnline</b> or 
      <b>ClusterResourceOffline</b> state.</li>
<li>The time limit stored in the resource's 
      <a href="/previous-versions/windows/desktop/mscs/resources-pendingtimeout">PendingTimeout</a> property has been 
      exceeded.</li>
</ul>
There is no need to call 
     <i>SetResourceStatus</i> to set the state of a resource to 
     a pending state because the Resource Monitor automatically sets it to the appropriate pending state whenever 
     <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> or 
     <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a> returns 
     <b>ERROR_IO_PENDING</b>.

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-clusworkerterminate">ClusWorkerTerminate</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>



<a href="/windows/desktop/api/resapi/ne-resapi-resource_exit_state">RESOURCE_EXIT_STATE</a>



<a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resource_status">RESOURCE_STATUS</a>



<a href="/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a>



<a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a>
