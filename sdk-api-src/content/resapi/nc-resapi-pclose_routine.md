---
UID: NC:resapi.PCLOSE_ROUTINE
title: PCLOSE_ROUTINE
author: windows-sdk-content
description: Closes a resource.
old-location: mscs\close.htm
tech.root: mscs
ms.assetid: c7c74440-c98a-4440-8bf4-10ebd1a68608
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: Close, PCLOSE_ROUTINE, PCLOSE_ROUTINE callback, PCLOSE_ROUTINE callback function [Failover Cluster], _wolf_close, mscs.close, resapi/PCLOSE_ROUTINE
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
 - PCLOSE_ROUTINE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PCLOSE_ROUTINE callback function


## -description


Closes a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The 
    <b>PCLOSE_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param Resource








#### - ResourceId [in]

Resource identifier of the resource to close.


## -returns



None. Call <a href="https://msdn.microsoft.com/d9da833f-36ca-4046-8d2f-cd4449dd3c63">SetLastError</a> to specify that an error has 
       occurred.




## -remarks



For effective implementation strategies of the <b>Close</b> 
     entry-point function, see 
     <a href="https://msdn.microsoft.com/b3f99392-1402-4c8d-b16b-e20bda4173da">Implementing Close</a>.


#### Examples

See <a href="mscs.resource_dll_examples">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

