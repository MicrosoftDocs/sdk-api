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

# RealTimeStylusLockType enumeration


## -description



Specifies the locks within the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object that protect the <b>RealTimeStylus Class</b> object's members and properties from modification.




## -enum-fields




### -field RTSLT_ObjLock

The object lock protects the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object's members and properties from modification.


### -field RTSLT_SyncEventLock

The object lock protects the synchronous plug-in collection from modification during event broadcasts.


### -field RTSLT_AsyncEventLock

The object lock protects the asynchronous plug-in collection from modification during event broadcasts.


### -field RTSLT_ExcludeCallback

The system excludes callbacks from the object's event or modification lock.


### -field RTSLT_SyncObjLock

The object lock protects the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> synchronous object's members and properties from modification.


### -field RTSLT_AsyncObjLock

The object lock protects the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> asynchronous object's members and properties from modification.


## -remarks



You can use these locks when you need to protect access to the plug-in collections or properties of the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object through the <a href="https://msdn.microsoft.com/fe76386d-55b5-40a8-aa6f-b4a1ee8d9fbd">IRealTimeStylusSynchronization Interface</a> interface.

For example, the window's handle can be locked to prevent it from being altered.




## -see-also




<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>



<a href="https://msdn.microsoft.com/a239b53c-7fc9-4211-962a-6cfbe0be4e4c">RealTimeStylus Reference</a>



<a href="https://msdn.microsoft.com/8baf8ee3-b6f7-4733-9e71-52627045c874">RealTimeStylus Structures</a>
 

 

