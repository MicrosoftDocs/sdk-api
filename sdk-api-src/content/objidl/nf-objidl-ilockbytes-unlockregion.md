---
UID: NF:objidl.ILockBytes.UnlockRegion
title: ILockBytes::UnlockRegion
author: windows-sdk-content
description: The UnlockRegion method removes the access restriction on a previously locked range of bytes.
old-location: stg\ilockbytes_unlockregion.htm
old-project: Stg
ms.assetid: 036ba242-8630-4013-860d-dd37919253be
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ILockBytes interface [Structured Storage],UnlockRegion method, ILockBytes.UnlockRegion, ILockBytes::UnlockRegion, UnlockRegion, UnlockRegion method [Structured Storage], UnlockRegion method [Structured Storage],ILockBytes interface, _stg_ilockbytes_unlockregion, objidl/ILockBytes::UnlockRegion, stg.ilockbytes_unlockregion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ILockBytes.UnlockRegion
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ILockBytes::UnlockRegion


## -description


The <b>UnlockRegion</b> method removes the access restriction on a previously locked range of bytes.


## -parameters




### -param libOffset [in]

Specifies the byte offset for the beginning of the range.


### -param cb [in]

Specifies, in bytes, the length of the range that is restricted.


### -param dwLockType [in]

Specifies the type of access restrictions previously placed on the range. This parameter uses a value from the 
<a href="https://msdn.microsoft.com/5d84fb08-aa4f-4918-a0de-550b02cb5287">LOCKTYPE</a> enumeration.


## -returns



This method can return one of these values.




## -remarks



<b>ILockBytes::UnlockRegion</b> unlocks a region previously locked with a call to 
<a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">ILockBytes::LockRegion</a>. Each region locked must be explicitly unlocked, using the same values for the <i>libOffset</i>, <i>cb</i>, and <i>dwLockType</i> parameters as in the matching calls to <b>ILockBytes::LockRegion</b>. Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.




## -see-also




<a href="https://msdn.microsoft.com/700b6a3c-1046-4c21-8887-16f344c23510">ILockBytes - File-Based Implementation</a>



<a href="https://msdn.microsoft.com/6ab019b0-34d7-4b6e-ba77-6b6881fabd29">ILockBytes - Global Memory Implementation</a>



<a href="https://msdn.microsoft.com/cea59e2a-99d8-472d-8e4f-2e2474789c20">ILockBytes::LockRegion</a>



<a href="https://msdn.microsoft.com/5d84fb08-aa4f-4918-a0de-550b02cb5287">LOCKTYPE</a>
 

 

