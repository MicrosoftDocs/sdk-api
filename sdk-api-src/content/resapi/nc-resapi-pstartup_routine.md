---
UID: NC:resapi.PSTARTUP_ROUTINE
title: PSTARTUP_ROUTINE (resapi.h)
description: Loads a resource DLL, returning a structure containing a function table and a version number.
helpviewer_keywords: ["PSTARTUP_ROUTINE","PSTARTUP_ROUTINE callback function [Failover Cluster]","Startup","Startup callback","Startup callback function [Failover Cluster]","_wolf_startup","mscs.startup","resapi/PSTARTUP_ROUTINE","resapi/Startup"]
old-location: mscs\startup.htm
tech.root: MsCS
ms.assetid: b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3
ms.date: 12/05/2018
ms.keywords: PSTARTUP_ROUTINE, PSTARTUP_ROUTINE callback function [Failover Cluster], Startup, Startup callback, Startup callback function [Failover Cluster], _wolf_startup, mscs.startup, resapi/PSTARTUP_ROUTINE, resapi/Startup
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
 - PSTARTUP_ROUTINE
 - resapi/PSTARTUP_ROUTINE
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
 - Startup
---

# PSTARTUP_ROUTINE callback function


## -description

Loads a <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a>, returning a structure 
    containing a function table and a version number. The <b>PSTARTUP_ROUTINE</b> 
    type defines a pointer to this function.

## -parameters

### -param ResourceType [in]

Type of resource being started.

### -param MinVersionSupported [in]

Minimum version of the <a href="/previous-versions/windows/desktop/mscs/resource-api">Resource API</a> supported by the 
       <a href="/previous-versions/windows/desktop/mscs/cluster-service">Cluster service</a>.

### -param MaxVersionSupported [in]

Maximum version of the Resource API supported by the Cluster service.

### -param SetResourceStatus [in]

Pointer to a callback function that the resource DLL should call to update its status after returning 
       <b>ERROR_IO_PENDING</b> from <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_routine">Online</a> or 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_routine">Offline</a>. For more information see 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pset_resource_status_routine">SetResourceStatus</a>.

### -param LogEvent [in]

Pointer to a callback function that the resource DLL should call to report events for the 
       <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. For more information see 
       <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plog_event_routine">LogEvent</a>.

### -param FunctionTable [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/resapi/ns-resapi-clres_function_table">CLRES_FUNCTION_TABLE</a> structure 
       that describes the Resource API version and the specific names for the entry points.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The request was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
<dt>1306 (0x51A)</dt>
</dl>
</td>
<td width="60%">
The resource DLL does not support a version that falls in the range identified by the 
         <i>MinVersionSupported</i> and <i>MaxVersionSupported</i> 
         parameters.

</td>
</tr>
</table>
 

If the operation was not successful, <i>Startup</i> should 
       return one of the <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

The <i>Startup</i> entry-point function returns a function table 
     that describes both the supported interface version of the Resource API and the entry points for all other 
     functions required by the supported version of the Resource API.

At present, only Resource API version 1.0 is supported.

If your resource supports more than one version of the Resource API, return a function table for the latest 
     version. The version number should be less than or equal to the <i>MaxVersionSupported</i> 
     parameter. If the version of the function table pointed to by the <i>FunctionTable</i> 
     parameter is not within range, your resource cannot be loaded successfully.

For more information see <a href="/previous-versions/windows/desktop/mscs/implementing-startup">Implementing Startup</a>.


#### Examples

See <a href="/previous-versions/windows/desktop/mscs/implementing-startup">Implementing Startup</a>.

<div class="code"></div>

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>
