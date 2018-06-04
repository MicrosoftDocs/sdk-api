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

# _ENTITY_METHOD callback function


## -description


The 
<b>RTM_ENTITY_EXPORT_METHOD</b> callback is the prototype for any method exported by a client.


## -parameters




### -param CallerHandle

Handle to the calling client.


### -param CalleeHandle

Handle to the client being called.


### -param *Input

Handle to the method to be invoked. Contains an input buffer.


### -param *Output

An array of 
<a href="https://msdn.microsoft.com/9ec05355-a912-4ed0-ace9-8823d333bab5">RTM_ENTITY_METHOD_OUTPUT</a> structures. Each structure consists of a (method identifier, correct output) tuple.


## -returns



This callback function does not return a value.




## -remarks



Methods can be exported when a client registers. Other clients, such as routing protocols, can invoke these methods to obtain client-specific information. For example, BGP can use a method to obtain OSFP information.




## -see-also




<a href="https://msdn.microsoft.com/1f900e85-c522-47c9-bfc8-5a1c1d01ab78">RTM_ENTITY_METHOD_INPUT</a>



<a href="https://msdn.microsoft.com/9ec05355-a912-4ed0-ace9-8823d333bab5">RTM_ENTITY_METHOD_OUTPUT</a>
 

 

