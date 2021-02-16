---
UID: NC:resapi.PIS_ALIVE_ROUTINE
title: PIS_ALIVE_ROUTINE (resapi.h)
description: Determines whether a resource is available for use.
helpviewer_keywords: ["IsAlive","IsAlive callback","IsAlive callback function [Failover Cluster]","PIS_ALIVE_ROUTINE","PIS_ALIVE_ROUTINE callback function [Failover Cluster]","_wolf_isalive","mscs.isalive","resapi/IsAlive","resapi/PIS_ALIVE_ROUTINE"]
old-location: mscs\isalive.htm
tech.root: MsCS
ms.assetid: ff7661af-0a24-4a2e-bb31-c967845a4ff4
ms.date: 12/05/2018
ms.keywords: IsAlive, IsAlive callback, IsAlive callback function [Failover Cluster], PIS_ALIVE_ROUTINE, PIS_ALIVE_ROUTINE callback function [Failover Cluster], _wolf_isalive, mscs.isalive, resapi/IsAlive, resapi/PIS_ALIVE_ROUTINE
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
 - PIS_ALIVE_ROUTINE
 - resapi/PIS_ALIVE_ROUTINE
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
 - IsAlive
---

# PIS_ALIVE_ROUTINE callback function


## -description

Determines whether a <a href="/previous-versions/windows/desktop/mscs/resources">resource</a> is available for 
    use. The <b>PIS_ALIVE_ROUTINE</b> type defines a pointer to this function.

## -parameters

### -param Resource [in]

Resource identifier for the resource to poll.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The resource is online and functioning properly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The resource is not functioning properly.

</td>
</tr>
</table>

## -remarks

For effective implementation strategies of the <i>IsAlive</i> 
     entry-point function, see <a href="/previous-versions/windows/desktop/mscs/implementing-isalive">Implementing IsAlive</a>.


#### Examples

See <a href="/previous-versions/aa372246(v=vs.85)">Resource DLL Examples</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>



<a href="/previous-versions/windows/desktop/mscs/resource-dll-entry-point-functions">Resource DLL Entry-Point Functions</a>