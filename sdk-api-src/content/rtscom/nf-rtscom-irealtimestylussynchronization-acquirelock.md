---
UID: NF:rtscom.IRealTimeStylusSynchronization.AcquireLock
title: IRealTimeStylusSynchronization::AcquireLock
author: windows-driver-content
description: Retrieves the specified lock.
old-location: tablet\irealtimestylussynchronization_acquirelock.htm
old-project: tablet
ms.assetid: 74e315c5-99c2-4ba5-bca5-72d812624fa0
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: 74e315c5-99c2-4ba5-bca5-72d812624fa0, AcquireLock, AcquireLock method [Tablet PC], AcquireLock method [Tablet PC],IRealTimeStylusSynchronization interface, IRealTimeStylusSynchronization interface [Tablet PC],AcquireLock method, IRealTimeStylusSynchronization.AcquireLock, IRealTimeStylusSynchronization::AcquireLock, rtscom/IRealTimeStylusSynchronization::AcquireLock, tablet.irealtimestylussynchronization_acquirelock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: StylusQueue
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RTSCom.dll
api_name:
-	IRealTimeStylusSynchronization.AcquireLock
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

