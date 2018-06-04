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

# IRealTimeStylusSynchronization::AcquireLock


## -description



Retrieves the specified lock.




## -parameters




### -param lock [in]

The <a href="https://msdn.microsoft.com/d472b588-b208-4665-9364-f2c92fe09bcd">RealTimeStylusLockType Enumeration</a> value that indicates which object lock to use.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Use the object locks to help protect the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object's members and properties from modification.




## -see-also




<a href="https://msdn.microsoft.com/fe76386d-55b5-40a8-aa6f-b4a1ee8d9fbd">IRealTimeStylusSynchronization Interface</a>



<a href="https://msdn.microsoft.com/13970fda-7b2a-4fb7-9403-8d9aad39d83a">IRealTimeStylusSynchronization::ReleaseLock Method</a>
 

 

