---
UID: NF:rtscom.IRealTimeStylusSynchronization.ReleaseLock
title: IRealTimeStylusSynchronization::ReleaseLock (rtscom.h)
description: Releases the specified lock.
helpviewer_keywords: ["13970fda-7b2a-4fb7-9403-8d9aad39d83a","IRealTimeStylusSynchronization interface [Tablet PC]","ReleaseLock method","IRealTimeStylusSynchronization.ReleaseLock","IRealTimeStylusSynchronization::ReleaseLock","ReleaseLock","ReleaseLock method [Tablet PC]","ReleaseLock method [Tablet PC]","IRealTimeStylusSynchronization interface","rtscom/IRealTimeStylusSynchronization::ReleaseLock","tablet.irealtimestylussynchronization_releaselock"]
old-location: tablet\irealtimestylussynchronization_releaselock.htm
tech.root: tablet
ms.assetid: 13970fda-7b2a-4fb7-9403-8d9aad39d83a
ms.date: 12/05/2018
ms.keywords: 13970fda-7b2a-4fb7-9403-8d9aad39d83a, IRealTimeStylusSynchronization interface [Tablet PC],ReleaseLock method, IRealTimeStylusSynchronization.ReleaseLock, IRealTimeStylusSynchronization::ReleaseLock, ReleaseLock, ReleaseLock method [Tablet PC], ReleaseLock method [Tablet PC],IRealTimeStylusSynchronization interface, rtscom/IRealTimeStylusSynchronization::ReleaseLock, tablet.irealtimestylussynchronization_releaselock
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
req.dll: RTSCom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRealTimeStylusSynchronization::ReleaseLock
 - rtscom/IRealTimeStylusSynchronization::ReleaseLock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylusSynchronization.ReleaseLock
---

# IRealTimeStylusSynchronization::ReleaseLock


## -description

Releases the specified lock.

## -parameters

### -param lock [in]

The <a href="/windows/desktop/api/rtscom/ne-rtscom-realtimestyluslocktype">RealTimeStylusLockType Enumeration</a> value that indicates which object lock to release.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

The object locks can be used to help protect the RealTimeStylus (RTS) object's members and properties from modification. The lock remains in effect until released.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylussynchronization">IRealTimeStylusSynchronization Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylussynchronization-acquirelock">IRealTimeStylusSynchronization::AcquireLock Method</a>