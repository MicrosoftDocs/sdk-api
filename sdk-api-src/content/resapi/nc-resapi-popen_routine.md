---
UID: NC:resapi.POPEN_ROUTINE
title: POPEN_ROUTINE
author: windows-sdk-content
description: Opens a resource.
old-location: mscs\open.htm
tech.root: MsCS
ms.assetid: 0a5c10c5-0380-4638-b49d-396be3b3c0dd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Open, Open callback, Open callback function [Failover Cluster], POPEN_ROUTINE, POPEN_ROUTINE callback function [Failover Cluster], _wolf_open, mscs.open, resapi/Open, resapi/POPEN_ROUTINE
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
 - Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# POPEN_ROUTINE callback function


## -description


Opens a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The 
    <b>POPEN_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param ResourceName [in]

Name of the resource to open.


### -param ResourceKey [in]


<a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">Cluster database</a> key for the 
       <a href="c_gly.htm">cluster</a> that includes the resource represented by 
       <i>ResourceName</i>.


### -param ResourceHandle [in]

Handle to be passed to the <a href="https://msdn.microsoft.com/8ddb4578-f8c4-462e-af04-8c537d585e8b">SetResourceStatus</a> 
       callback function in the <a href="https://msdn.microsoft.com/b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3">Startup</a> entry-point function.


## -returns



If the operation was successful, <i>Open</i> returns a resource 
       identifier (<b>RESID</b>).

If the operation was not successful, <i>Open</i> returns 
       <b>NULL</b>. Call  <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to 
       specify that an error has occurred.




## -remarks



The <i>Open</i> entry-point function opens a resource with the name 
     identified by the <i>ResourceName</i> parameter and returns its resource identifier. The 
     resource identifier can be used in future calls to other 
     <a href="https://msdn.microsoft.com/764a35dd-a681-4af0-8e2c-281a254a3a30">Resource API</a> entry points to identify the resource.

Never close the handle represented by the <i>ResourceHandle</i> parameter or use it for any 
     purpose other than passing it to the <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> 
     through either the <a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a> callback function or the 
     <a href="https://msdn.microsoft.com/8ddb4578-f8c4-462e-af04-8c537d585e8b">SetResourceStatus</a> callback function.

For effective implementation strategies of the <i>Open</i> 
     entry-point function, see <a href="https://msdn.microsoft.com/ba8733dc-ec22-4e21-ab21-a7cbf89273e4">Implementing Open</a>.


#### Examples

See <a href="mscs.resource_dll_examples">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/91389083-e007-4d64-885f-e5188e74b9d8">LogEvent</a>



<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>



<a href="https://msdn.microsoft.com/8ddb4578-f8c4-462e-af04-8c537d585e8b">SetResourceStatus</a>
 

 

