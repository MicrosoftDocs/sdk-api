---
UID: NC:resapi.PSET_RESOURCE_STATUS_ROUTINE_EX
title: PSET_RESOURCE_STATUS_ROUTINE_EX (resapi.h)
description: The PSET_RESOURCE_STATUS_ROUTINE_EX callback function is called to update the status of a resource. (PSET_RESOURCE_STATUS_ROUTINE_EX)
helpviewer_keywords: ["PSET_RESOURCE_STATUS_ROUTINE_EX","PSET_RESOURCE_STATUS_ROUTINE_EX callback function [Failover Cluster]","SetResourceStatusEx","SetResourceStatusEx callback","SetResourceStatusEx callback function [Failover Cluster]","mscs.setresourcestatusex","resapi/PSET_RESOURCE_STATUS_ROUTINE_EX","resapi/SetResourceStatusEx"]
old-location: mscs\setresourcestatusex.htm
tech.root: MsCS
ms.assetid: 3733F912-9D43-489B-91D8-7128D0F5D1A4
ms.date: 08/03/2022
ms.keywords: PSET_RESOURCE_STATUS_ROUTINE_EX, PSET_RESOURCE_STATUS_ROUTINE_EX callback function [Failover Cluster], SetResourceStatusEx, SetResourceStatusEx callback, SetResourceStatusEx callback function [Failover Cluster], mscs.setresourcestatusex, resapi/PSET_RESOURCE_STATUS_ROUTINE_EX, resapi/SetResourceStatusEx
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - PSET_RESOURCE_STATUS_ROUTINE_EX
 - resapi/PSET_RESOURCE_STATUS_ROUTINE_EX
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
 - SetResourceStatusEx
---

# PSET_RESOURCE_STATUS_ROUTINE_EX callback function


## -description

Called to update the status of a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. 
    The <b>PSET_RESOURCE_STATUS_ROUTINE_EX</b> type defines a pointer to this function.

## -parameters

### -param ResourceHandle

A handle to the resource to be updated. The <i>ResourceHandle</i> parameter should 
       contain the same handle that is used for the <i>ResourceHandle</i> parameter in the 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_v2_routine">OpenV2</a> entry point for this resource.

### -param ResourceStatus

A pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-resource_status_ex">RESOURCE_STATUS_EX</a> structure that 
       contains information about the resource's state.

## -returns

One of 
       the following values of the 
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
The resource has not been terminated. Worker threads can  continue 
         <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_v2_routine">OnlineV2</a> and 
         <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_v2_routine">OfflineV2</a> operations for the resource.

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
         <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_v2_routine">OnlineV2</a> or 
         <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_v2_routine">OfflineV2</a> operations and immediately terminate all worker 
         threads that are assigned to the resource.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>
