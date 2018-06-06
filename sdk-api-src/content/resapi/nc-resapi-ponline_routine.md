---
UID: NC:resapi.PONLINE_ROUTINE
title: PONLINE_ROUTINE
author: windows-sdk-content
description: Marks a resource as available for use.
old-location: mscs\online.htm
old-project: MsCS
ms.assetid: b406ef44-0622-4625-a6cf-462b6ea6018d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: Online, Online callback, Online callback function [Failover Cluster], PONLINE_ROUTINE, PONLINE_ROUTINE callback function [Failover Cluster], _wolf_online, mscs.online, resapi/Online, resapi/PONLINE_ROUTINE
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
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
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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

See <a href="mscs.resource_dll_examples">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a>



<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

