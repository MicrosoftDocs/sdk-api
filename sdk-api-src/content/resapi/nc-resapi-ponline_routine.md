---
UID: NC:resapi.PONLINE_ROUTINE
title: PONLINE_ROUTINE (resapi.h)
description: The PONLINE_ROUTINE callback function marks a resource as available for use. (PONLINE_ROUTINE)
helpviewer_keywords: ["Online","Online callback","Online callback function [Failover Cluster]","PONLINE_ROUTINE","PONLINE_ROUTINE callback function [Failover Cluster]","_wolf_online","mscs.online","resapi/Online","resapi/PONLINE_ROUTINE"]
old-location: mscs\online.htm
tech.root: MsCS
ms.assetid: b406ef44-0622-4625-a6cf-462b6ea6018d
ms.date: 08/03/2022
ms.keywords: Online, Online callback, Online callback function [Failover Cluster], PONLINE_ROUTINE, PONLINE_ROUTINE callback function [Failover Cluster], _wolf_online, mscs.online, resapi/Online, resapi/PONLINE_ROUTINE
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
 - PONLINE_ROUTINE
 - resapi/PONLINE_ROUTINE
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
 - Online
---

# PONLINE_ROUTINE callback function


## -description

Marks a 
    <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> as available for use. The 
    <b>PONLINE_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param Resource [in]

Resource identifier for the resource to be made available.

### -param EventHandle [in, out]

On input, <i>EventHandle</i> is <b>NULL</b>. On output, 
       <i>EventHandle</i> contains a handle to a nonsignaled 
       <a href="/windows/desktop/Sync/synchronization-objects">synchronization object</a>. The 
       <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> can signal this handle at any time to report 
       a resource failure to the <a href="/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a>. 
       <i>EventHandle</i> can also be set to <b>NULL</b> on output, indicating 
       that the resource does not support asynchronous event notification.

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
The operation was successful, and the resource is now 
         <a href="/previous-versions/windows/desktop/mscs/o-gly">online</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_NOT_AVAILABLE</b></dt>
<dt>5006 (0x138E)</dt>
</dl>
</td>
<td width="60%">
The resource was arbitrated with some other systems, and one of the other systems won the arbitration. Only 
         <a href="/previous-versions/windows/desktop/mscs/q-gly">quorum-capable resources</a> return this 
         value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
<dt>997 (0x3E5)</dt>
</dl>
</td>
<td width="60%">
The request is pending, and a thread has been activated to process the online request.

</td>
</tr>
</table>
 

If the operation was not successful for other reasons, 
       <i>Online</i> should return one of the 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

If the <b>Online</b> entry-point function returns an error code 
     other than <b>ERROR_IO_PENDING</b>, the Resource Monitor logs an event and calls 
     <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a>.

Returning a valid <i>EventHandle</i> yields the following benefits:

<ul>
<li>The Resource Monitor will not perform <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-plooks_alive_routine">LooksAlive</a> 
      polling. Avoiding this overhead is often useful, particularly when your DLL supports multiple resource 
      instances.</li>
<li>You can report resource failure at any time by signaling the handle. The Resource Monitor will immediately 
      call <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pis_alive_routine">IsAlive</a> to verify that the resource has failed.</li>
</ul>
For effective implementation strategies of the <i>Online</i> 
    entry-point function, see <a href="/previous-versions/windows/desktop/mscs/implementing-online">Implementing Online</a>.


#### Examples

See <a href="/previous-versions/aa372246(v=vs.85)">Resource DLL Examples</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a>



<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>
