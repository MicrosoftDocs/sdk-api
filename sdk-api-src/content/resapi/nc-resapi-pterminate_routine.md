---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
     <a href="https://msdn.microsoft.com/library/windows/hardware/dn997353">Online</a> or 
     <a href="https://msdn.microsoft.com/library/windows/hardware/dn997350">Offline</a> request for the resource, these requests are canceled 
     and the resource is taken offline immediately.

For effective implementation strategies of the <i>Terminate</i> 
     entry-point function, see 
     <a href="https://msdn.microsoft.com/df6edc61-d325-46a5-b486-079a52dfaf77">Implementing Terminate</a>.


#### Examples

See <a href="mscs.resource_dll_examples">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

