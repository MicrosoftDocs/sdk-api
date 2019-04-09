---
UID: NE:rtscom.RealTimeStylusLockType
title: RealTimeStylusLockType (rtscom.h)
author: windows-sdk-content
description: Specifies the locks within the RealTimeStylus Class object that protect the RealTimeStylus Class object's members and properties from modification.
old-location: tablet\realtimestyluslocktype.htm
tech.root: tablet
ms.assetid: d472b588-b208-4665-9364-f2c92fe09bcd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RTSLT_AsyncEventLock, RTSLT_AsyncObjLock, RTSLT_ExcludeCallback, RTSLT_ObjLock, RTSLT_SyncEventLock, RTSLT_SyncObjLock, RealTimeStylusLockType, RealTimeStylusLockType enumeration [Tablet PC], d472b588-b208-4665-9364-f2c92fe09bcd, rtscom/RTSLT_AsyncEventLock, rtscom/RTSLT_AsyncObjLock, rtscom/RTSLT_ExcludeCallback, rtscom/RTSLT_ObjLock, rtscom/RTSLT_SyncEventLock, rtscom/RTSLT_SyncObjLock, rtscom/RealTimeStylusLockType, tablet.realtimestyluslocktype
ms.topic: enum
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
 - HeaderDef
api_location:
 - RTSCom.h
api_name:
 - RealTimeStylusLockType
product: Windows
targetos: Windows
req.typenames: RealTimeStylusLockType
req.redist: 
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
 

 

