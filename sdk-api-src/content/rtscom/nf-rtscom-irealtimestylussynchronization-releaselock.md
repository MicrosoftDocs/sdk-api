---
UID: NF:rtscom.IRealTimeStylusSynchronization.ReleaseLock
title: IRealTimeStylusSynchronization::ReleaseLock
author: windows-sdk-content
description: Releases the specified lock.
old-location: tablet\irealtimestylussynchronization_releaselock.htm
old-project: tablet
ms.assetid: 13970fda-7b2a-4fb7-9403-8d9aad39d83a
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: 13970fda-7b2a-4fb7-9403-8d9aad39d83a, IRealTimeStylusSynchronization interface [Tablet PC],ReleaseLock method, IRealTimeStylusSynchronization.ReleaseLock, IRealTimeStylusSynchronization::ReleaseLock, ReleaseLock, ReleaseLock method [Tablet PC], ReleaseLock method [Tablet PC],IRealTimeStylusSynchronization interface, rtscom/IRealTimeStylusSynchronization::ReleaseLock, tablet.irealtimestylussynchronization_releaselock
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: StylusQueue
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylusSynchronization.ReleaseLock
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IRealTimeStylusSynchronization::ReleaseLock


## -description



Releases the specified lock.




## -parameters




### -param lock [in]

The <a href="https://msdn.microsoft.com/d472b588-b208-4665-9364-f2c92fe09bcd">RealTimeStylusLockType Enumeration</a> value that indicates which object lock to release.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The object locks can be used to help protect the RealTimeStylus (RTS) object's members and properties from modification. The lock remains in effect until released.




## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/fe76386d-55b5-40a8-aa6f-b4a1ee8d9fbd">IRealTimeStylusSynchronization Interface</a>



<a href="https://msdn.microsoft.com/74e315c5-99c2-4ba5-bca5-72d812624fa0">IRealTimeStylusSynchronization::AcquireLock Method</a>
 

 

