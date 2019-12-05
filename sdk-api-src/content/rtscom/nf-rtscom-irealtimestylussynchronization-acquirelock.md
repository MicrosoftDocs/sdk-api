---
UID: NF:rtscom.IRealTimeStylusSynchronization.AcquireLock
title: IRealTimeStylusSynchronization::AcquireLock (rtscom.h)
description: Retrieves the specified lock.
old-location: tablet\irealtimestylussynchronization_acquirelock.htm
tech.root: tablet
ms.assetid: 74e315c5-99c2-4ba5-bca5-72d812624fa0
ms.date: 12/05/2018
ms.keywords: 74e315c5-99c2-4ba5-bca5-72d812624fa0, AcquireLock, AcquireLock method [Tablet PC], AcquireLock method [Tablet PC],IRealTimeStylusSynchronization interface, IRealTimeStylusSynchronization interface [Tablet PC],AcquireLock method, IRealTimeStylusSynchronization.AcquireLock, IRealTimeStylusSynchronization::AcquireLock, rtscom/IRealTimeStylusSynchronization::AcquireLock, tablet.irealtimestylussynchronization_acquirelock
ms.topic: method
f1_keywords:
- rtscom/IRealTimeStylusSynchronization.AcquireLock
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- RTSCom.dll
api_name:
- IRealTimeStylusSynchronization.AcquireLock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRealTimeStylusSynchronization::AcquireLock


## -description



Retrieves the specified lock.




## -parameters




### -param lock [in]

The <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/ne-rtscom-realtimestyluslocktype">RealTimeStylusLockType Enumeration</a> value that indicates which object lock to use.


## -returns



For a description of the return values, see <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Use the object locks to help protect the <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object's members and properties from modification.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-irealtimestylussynchronization">IRealTimeStylusSynchronization Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-irealtimestylussynchronization-releaselock">IRealTimeStylusSynchronization::ReleaseLock Method</a>
 

 

