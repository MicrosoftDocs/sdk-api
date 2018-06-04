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

# PARBITRATE_ROUTINE callback function


## -description


Allows a <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> to attempt to regain ownership of a 
    <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a>. The 
    <b>PARBITRATE_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param Resource [in]

Resource identifier for the quorum resource to be owned.


### -param LostQuorumResource [in]

Address of a <a href="https://msdn.microsoft.com/353eaf47-f93e-4243-8bed-7b6f07513a3c">QuorumResourceLost</a> callback 
       function that should be called if control of the quorum resource is lost after being successfully gained.


## -returns





Returns DWORD that ...






## -remarks



The <i>Arbitrate</i> entry-point function is implemented for 
     <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resources</a> only. Expect this function to 
     be called only after both <a href="https://msdn.microsoft.com/b07a2c32-2ff5-4917-9bcb-e1cfe445b3b3">Startup</a> and 
     <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> have been called.

Implementations of <b>Arbitrate</b> should take less than 300 
     milliseconds to complete.

If <b>Arbitrate</b> is successful, make sure that only the 
     current node can successfully arbitrate for the quorum resource represented by 
     <i>ResourceId</i>. For example, a disk resource can implement a defense by continually 
     replacing the reservation made on it once per second.




## -see-also




<a href="https://msdn.microsoft.com/933d7b97-b5be-4c84-a983-41d1fd935c19">Resource DLL Entry-Point Functions</a>
 

 

