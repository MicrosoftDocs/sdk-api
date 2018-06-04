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

# IBroadcastEventEx::FireEx


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>FireEx</b> method fires a broadcast event.


## -parameters




### -param EventID [in]

GUID that specifies the event.


### -param Param1 [in]

Specifies the first implementation-dependent parameter.


### -param Param2 [in]

Specifies the second implementation-dependent parameter.


### -param Param3 [in]

Specifies the third implementation-dependent parameter.


### -param Param4 [in]

Specifies the fourth implementation-dependent parameter.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is similar to <a href="https://msdn.microsoft.com/974b42d7-bf68-426b-a146-4e520cac3274">IBroadcastEvent::Fire</a>, but it includes four additional parameters for passing implementation-dependent information between the object that fires the event and the objects that wait on the event. The designer who implements the objects must determine what meaning, if any, to assign to these parameters.




## -see-also




<a href="https://msdn.microsoft.com/c16ad538-afc6-4530-a2fd-18965b63983b">IBroadcastEventEx Interface</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

