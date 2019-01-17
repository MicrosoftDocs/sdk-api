---
UID: NC:resapi.PIS_ALIVE_ROUTINE
title: PIS_ALIVE_ROUTINE
author: windows-sdk-content
description: Determines whether a resource is available for use.
old-location: mscs\isalive.htm
tech.root: MsCS
ms.assetid: ff7661af-0a24-4a2e-bb31-c967845a4ff4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IsAlive, IsAlive callback, IsAlive callback function [Failover Cluster], PIS_ALIVE_ROUTINE, PIS_ALIVE_ROUTINE callback function [Failover Cluster], _wolf_isalive, mscs.isalive, resapi/IsAlive, resapi/PIS_ALIVE_ROUTINE
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
 - IsAlive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIS_ALIVE_ROUTINE callback function


## -description


Determines whether a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> is available for 
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
     entry-point function, see <a href="https://msdn.microsoft.com/f552b41e-d587-4028-9b6e-394c071d0994">Implementing IsAlive</a>.


#### Examples

See <a href="https://msdn.microsoft.com/library/Aa372246(v=VS.85).aspx">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a>



<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

