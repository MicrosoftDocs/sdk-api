---
UID: NF:rtscom.IRealTimeStylusSynchronization.AcquireLock
title: IRealTimeStylusSynchronization::AcquireLock (rtscom.h)
description: Retrieves the specified lock.
helpviewer_keywords: ["74e315c5-99c2-4ba5-bca5-72d812624fa0","AcquireLock","AcquireLock method [Tablet PC]","AcquireLock method [Tablet PC]","IRealTimeStylusSynchronization interface","IRealTimeStylusSynchronization interface [Tablet PC]","AcquireLock method","IRealTimeStylusSynchronization.AcquireLock","IRealTimeStylusSynchronization::AcquireLock","rtscom/IRealTimeStylusSynchronization::AcquireLock","tablet.irealtimestylussynchronization_acquirelock"]
old-location: tablet\irealtimestylussynchronization_acquirelock.htm
tech.root: tablet
ms.assetid: 74e315c5-99c2-4ba5-bca5-72d812624fa0
ms.date: 12/05/2018
ms.keywords: 74e315c5-99c2-4ba5-bca5-72d812624fa0, AcquireLock, AcquireLock method [Tablet PC], AcquireLock method [Tablet PC],IRealTimeStylusSynchronization interface, IRealTimeStylusSynchronization interface [Tablet PC],AcquireLock method, IRealTimeStylusSynchronization.AcquireLock, IRealTimeStylusSynchronization::AcquireLock, rtscom/IRealTimeStylusSynchronization::AcquireLock, tablet.irealtimestylussynchronization_acquirelock
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
 - IRealTimeStylusSynchronization::AcquireLock
 - rtscom/IRealTimeStylusSynchronization::AcquireLock
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
 - IRealTimeStylusSynchronization.AcquireLock
---

# IRealTimeStylusSynchronization::AcquireLock


## -description

Retrieves the specified lock.

## -parameters

### -param lock [in]

The <a href="/windows/desktop/api/rtscom/ne-rtscom-realtimestyluslocktype">RealTimeStylusLockType Enumeration</a> value that indicates which object lock to use.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

Use the object locks to help protect the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object's members and properties from modification.

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylussynchronization">IRealTimeStylusSynchronization Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylussynchronization-releaselock">IRealTimeStylusSynchronization::ReleaseLock Method</a>