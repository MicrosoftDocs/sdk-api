---
UID: NC:resapi.PONLINE_ROUTINE
title: PONLINE_ROUTINE
author: windows-sdk-content
description: Marks a resource as available for use.
old-location: mscs\online.htm
tech.root: mscs
ms.assetid: b406ef44-0622-4625-a6cf-462b6ea6018d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Online, Online callback, Online callback function [Failover Cluster], PONLINE_ROUTINE, PONLINE_ROUTINE callback function [Failover Cluster], _wolf_online, mscs.online, resapi/Online, resapi/PONLINE_ROUTINE
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - Online
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PONLINE_ROUTINE callback function


## -description


Marks a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> as available for use. The 
    <b>PONLINE_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param Resource [in]

Resource identifier for the resource to be made available.


### -param EventHandle [in, out]

On input, <i>EventHandle</i> is <b>NULL</b>. On output, 
       <i>EventHandle</i> contains a handle to a nonsignaled 
       <a href="https://msdn.microsoft.com/11558ae9-1056-48bf-96f5-94a051df41c3">synchronization object</a>. The 
       <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> can signal this handle at any time to report 
       a resource failure to the <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a>. 
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
         <a href="https://msdn.microsoft.com/en-us/library/Aa371781(v=VS.85).aspx">online</a>.

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
         <a href="https://msdn.microsoft.com/en-us/library/Aa371820(v=VS.85).aspx">quorum-capable resources</a> return this 
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
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



If the <b>Online</b> entry-point function returns an error code 
     other than <b>ERROR_IO_PENDING</b>, the Resource Monitor logs an event and calls 
     <a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>.

Returning a valid <i>EventHandle</i> yields the following benefits:

<ul>
<li>The Resource Monitor will not perform <a href="https://msdn.microsoft.com/cfc57325-847d-4f59-bee8-6a02b0a2ef32">LooksAlive</a> 
      polling. Avoiding this overhead is often useful, particularly when your DLL supports multiple resource 
      instances.</li>
<li>You can report resource failure at any time by signaling the handle. The Resource Monitor will immediately 
      call <a href="https://msdn.microsoft.com/ff7661af-0a24-4a2e-bb31-c967845a4ff4">IsAlive</a> to verify that the resource has failed.</li>
</ul>
For effective implementation strategies of the <i>Online</i> 
    entry-point function, see <a href="https://msdn.microsoft.com/888a973f-2b1f-46d2-abcc-f87e62ffbd4b">Implementing Online</a>.


#### Examples

See <a href="https://msdn.microsoft.com/library/Aa372246(v=VS.85).aspx">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a>



<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

