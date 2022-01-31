---
UID: NE:rtscom.RealTimeStylusLockType
title: RealTimeStylusLockType (rtscom.h)
description: Specifies the locks within the RealTimeStylus Class object that protect the RealTimeStylus Class object's members and properties from modification.
helpviewer_keywords: ["RTSLT_AsyncEventLock","RTSLT_AsyncObjLock","RTSLT_ExcludeCallback","RTSLT_ObjLock","RTSLT_SyncEventLock","RTSLT_SyncObjLock","RealTimeStylusLockType","RealTimeStylusLockType enumeration [Tablet PC]","d472b588-b208-4665-9364-f2c92fe09bcd","rtscom/RTSLT_AsyncEventLock","rtscom/RTSLT_AsyncObjLock","rtscom/RTSLT_ExcludeCallback","rtscom/RTSLT_ObjLock","rtscom/RTSLT_SyncEventLock","rtscom/RTSLT_SyncObjLock","rtscom/RealTimeStylusLockType","tablet.realtimestyluslocktype"]
old-location: tablet\realtimestyluslocktype.htm
tech.root: tablet
ms.assetid: d472b588-b208-4665-9364-f2c92fe09bcd
ms.date: 12/05/2018
ms.keywords: RTSLT_AsyncEventLock, RTSLT_AsyncObjLock, RTSLT_ExcludeCallback, RTSLT_ObjLock, RTSLT_SyncEventLock, RTSLT_SyncObjLock, RealTimeStylusLockType, RealTimeStylusLockType enumeration [Tablet PC], d472b588-b208-4665-9364-f2c92fe09bcd, rtscom/RTSLT_AsyncEventLock, rtscom/RTSLT_AsyncObjLock, rtscom/RTSLT_ExcludeCallback, rtscom/RTSLT_ObjLock, rtscom/RTSLT_SyncEventLock, rtscom/RTSLT_SyncObjLock, rtscom/RealTimeStylusLockType, tablet.realtimestyluslocktype
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
targetos: Windows
req.typenames: RealTimeStylusLockType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RealTimeStylusLockType
 - rtscom/RealTimeStylusLockType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - RTSCom.h
api_name:
 - RealTimeStylusLockType
---

# RealTimeStylusLockType enumeration


## -description

Specifies the locks within the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that protect the <b>RealTimeStylus Class</b> object's members and properties from modification.

## -enum-fields

### -field RTSLT_ObjLock:0x1

The object lock protects the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object's members and properties from modification.

### -field RTSLT_SyncEventLock:0x2

The object lock protects the synchronous plug-in collection from modification during event broadcasts.

### -field RTSLT_AsyncEventLock:0x4

The object lock protects the asynchronous plug-in collection from modification during event broadcasts.

### -field RTSLT_ExcludeCallback:0x8

The system excludes callbacks from the object's event or modification lock.

### -field RTSLT_SyncObjLock:0xb

The object lock protects the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> synchronous object's members and properties from modification.

### -field RTSLT_AsyncObjLock:0xd

The object lock protects the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> asynchronous object's members and properties from modification.

## -remarks

You can use these locks when you need to protect access to the plug-in collections or properties of the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object through the <a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylussynchronization">IRealTimeStylusSynchronization Interface</a> interface.

For example, the window's handle can be locked to prevent it from being altered.

## -see-also

<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>



<a href="/windows/desktop/tablet/realtimestylus-reference">RealTimeStylus Reference</a>



<a href="/windows/desktop/tablet/realtimestylus-structures">RealTimeStylus Structures</a>
