---
UID: NC:resapi.POFFLINE_ROUTINE
title: POFFLINE_ROUTINE (resapi.h)
description: The POFFLINE_ROUTINE callback function marks a resource as unavailable for use after cleanup processing is complete.
helpviewer_keywords: ["Offline","Offline callback","Offline callback function [Failover Cluster]","POFFLINE_ROUTINE","POFFLINE_ROUTINE callback function [Failover Cluster]","_wolf_offline","mscs.offline","resapi/Offline","resapi/POFFLINE_ROUTINE"]
old-location: mscs\offline.htm
tech.root: MsCS
ms.assetid: 1d67a4f5-66f8-4818-8b63-d0f50452f889
ms.date: 08/03/2022
ms.keywords: Offline, Offline callback, Offline callback function [Failover Cluster], POFFLINE_ROUTINE, POFFLINE_ROUTINE callback function [Failover Cluster], _wolf_offline, mscs.offline, resapi/Offline, resapi/POFFLINE_ROUTINE
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
 - POFFLINE_ROUTINE
 - resapi/POFFLINE_ROUTINE
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
 - Offline
---

# POFFLINE_ROUTINE callback function


## -description

Marks a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> as unavailable for use after cleanup 
    processing is complete. The <b>POFFLINE_ROUTINE</b> type defines a pointer to 
    this function.

## -parameters

### -param Resource [in]

Resource identifier for the resource to be taken offline.

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
The request completed successfully, and the resource is offline.

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
The request is still pending, and a thread has been activated to process the offline request.

</td>
</tr>
</table>
 

If the operation was not successful for other reasons, 
       <i>Offline</i> should return one of the 
       <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

If <i>Offline</i> returns an error code other than 
     <b>ERROR_IO_PENDING</b>, the 
     <a href="/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a> logs an event and calls 
     <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a>.

For effective implementation strategies of the <i>Offline</i> 
     entry-point function, see <a href="/previous-versions/windows/desktop/mscs/implementing-offline">Implementing Offline</a>.


#### Examples

See <a href="/previous-versions/aa372246(v=vs.85)">Resource DLL Examples</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedel">NetShareDel</a>



<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry Point Functions</a>
