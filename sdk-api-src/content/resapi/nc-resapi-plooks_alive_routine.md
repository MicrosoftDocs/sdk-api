---
UID: NC:resapi.PLOOKS_ALIVE_ROUTINE
title: PLOOKS_ALIVE_ROUTINE
author: windows-sdk-content
description: Determines whether a resource appears to be available for use.
old-location: mscs\looksalive.htm
tech.root: MsCS
ms.assetid: cfc57325-847d-4f59-bee8-6a02b0a2ef32
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LooksAlive, LooksAlive callback, LooksAlive callback function [Failover Cluster], PLOOKS_ALIVE_ROUTINE, PLOOKS_ALIVE_ROUTINE callback function [Failover Cluster], _wolf_looksalive, mscs.looksalive, resapi/LooksAlive, resapi/PLOOKS_ALIVE_ROUTINE
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
 - LooksAlive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PLOOKS_ALIVE_ROUTINE callback function


## -description


Determines whether a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> appears to be available 
    for use. The <b>PLOOKS_ALIVE_ROUTINE</b> type defines a pointer to this 
    function.


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
The resource is probably online and available for use.

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
The resource may not be functioning properly.

</td>
</tr>
</table>
 




## -remarks



For effective implementation strategies of the 
     <i>LooksAlive</i> entry-point function, see 
     <a href="https://msdn.microsoft.com/436d99c7-91ab-4ecd-9ee3-f42887c00407">Implementing LooksAlive</a>.


#### Examples

See <a href="https://msdn.microsoft.com/library/Aa372246(v=VS.85).aspx">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

