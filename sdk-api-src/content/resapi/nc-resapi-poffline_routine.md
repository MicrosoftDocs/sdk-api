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

# POFFLINE_ROUTINE callback function


## -description


Marks a <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> as unavailable for use after cleanup 
    processing is complete. The <b>POFFLINE_ROUTINE</b> type defines a pointer to 
    this function.


## -parameters




### -param Resource [in]

Resource identifier for the resource to be taken offline.


## -returns



If the operation was not successful for other reasons, 
       <i>Offline</i> should return one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



If <i>Offline</i> returns an error code other than 
     <b>ERROR_IO_PENDING</b>, the 
     <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> logs an event and calls 
     <a href="https://msdn.microsoft.com/b53ab7db-ed17-4386-8a5f-5d0b0d1cb1b3">Terminate</a>.

For effective implementation strategies of the <i>Offline</i> 
     entry-point function, see <a href="https://msdn.microsoft.com/d6459783-cb94-4fbc-b76d-da811db379ce">Implementing Offline</a>.


#### Examples

See <a href="mscs.resource_dll_examples">Resource DLL Examples</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/374b8f81-b3d6-4967-bd4a-ffd3fdc3cf7c">NetShareDel</a>



<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry Point Functions</a>
 

 

