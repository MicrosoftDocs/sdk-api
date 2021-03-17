---
UID: NC:resapi.PARBITRATE_ROUTINE
title: PARBITRATE_ROUTINE (resapi.h)
description: Allows a node to attempt to regain ownership of a quorum resource.
helpviewer_keywords: ["Arbitrate","Arbitrate callback","Arbitrate callback function [Failover Cluster]","PARBITRATE_ROUTINE","PARBITRATE_ROUTINE callback function [Failover Cluster]","_wolf_arbitrate","mscs.arbitrate","resapi/Arbitrate","resapi/PARBITRATE_ROUTINE"]
old-location: mscs\arbitrate.htm
tech.root: MsCS
ms.assetid: dc16b785-bbb1-4917-a826-e49445a86c26
ms.date: 12/05/2018
ms.keywords: Arbitrate, Arbitrate callback, Arbitrate callback function [Failover Cluster], PARBITRATE_ROUTINE, PARBITRATE_ROUTINE callback function [Failover Cluster], _wolf_arbitrate, mscs.arbitrate, resapi/Arbitrate, resapi/PARBITRATE_ROUTINE
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
 - PARBITRATE_ROUTINE
 - resapi/PARBITRATE_ROUTINE
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
 - Arbitrate
---

# PARBITRATE_ROUTINE callback function


## -description

Allows a <a href="/previous-versions/windows/desktop/mscs/nodes">node</a> to attempt to regain ownership of a 
    <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resource</a>. The 
    <b>PARBITRATE_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param Resource [in]

Resource identifier for the quorum resource to be owned.

### -param LostQuorumResource [in]

Address of a <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pquorum_resource_lost">QuorumResourceLost</a> callback 
       function that should be called if control of the quorum resource is lost after being successfully gained.

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
The arbitration was successful and the quorum resource remains defended.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><a href="/windows/desktop/Debug/system-error-codes">Error code</a></b></dt>
</dl>
</td>
<td width="60%">
The arbitration was not successful.

</td>
</tr>
</table>

## -remarks

The <i>Arbitrate</i> entry-point function is implemented for 
     <a href="/previous-versions/windows/desktop/mscs/quorum-resource">quorum resources</a> only. Expect this function to 
     be called only after both <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a> and 
     <a href="/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> have been called.

Implementations of <b>Arbitrate</b> should take less than 300 
     milliseconds to complete.

If <b>Arbitrate</b> is successful, make sure that only the 
     current node can successfully arbitrate for the quorum resource represented by 
     <i>ResourceId</i>. For example, a disk resource can implement a defense by continually 
     replacing the reservation made on it once per second.

## -see-also

<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>