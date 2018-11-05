---
UID: NC:resapi.PTERMINATE_ROUTINE
title: PTERMINATE_ROUTINE
author: windows-sdk-content
description: Immediately marks a resource as unavailable for use without waiting for cleanup processing to be completed.
old-location: mscs\terminate.htm
tech.root: MsCS
ms.assetid: b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PTERMINATE_ROUTINE, PTERMINATE_ROUTINE callback function [Failover Cluster], Terminate, Terminate callback, Terminate callback function [Failover Cluster], _wolf_terminate, mscs.terminate, resapi/PTERMINATE_ROUTINE, resapi/Terminate
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
 - Terminate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PTERMINATE_ROUTINE callback function


## -description


Immediately marks a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> as unavailable for use 
    without waiting for cleanup processing to be completed. The 
    <b>PTERMINATE_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param Resource [in]

Resource identifier for the resource to be made unavailable.


## -returns



This callback function does not return a value.




## -remarks



The <i>Terminate</i> entry-point function instantly marks a 
     resource as unavailable for use. If there is a thread processing an 
     <a href="https://msdn.microsoft.com/b406ef44-0622-4625-a6cf-462b6ea6018d">Online</a> or 
     <a href="https://msdn.microsoft.com/1d67a4f5-66f8-4818-8b63-d0f50452f889">Offline</a> request for the resource, these requests are canceled 
     and the resource is taken offline immediately.

For effective implementation strategies of the <i>Terminate</i> 
     entry-point function, see 
     <a href="https://msdn.microsoft.com/df6edc61-d325-46a5-b486-079a52dfaf77">Implementing Terminate</a>.


#### Examples

See <a href="mscs.resource_dll_examples">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

