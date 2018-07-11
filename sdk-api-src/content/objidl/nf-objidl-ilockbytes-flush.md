---
UID: NF:objidl.ILockBytes.Flush
title: ILockBytes::Flush
author: windows-sdk-content
description: The Flush method ensures that any internal buffers maintained by the ILockBytes implementation are written out to the underlying physical storage.
old-location: stg\ilockbytes_flush.htm
old-project: stg
ms.assetid: 9396c44f-ad76-49f4-9796-d29570466a27
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: Flush, Flush method [Structured Storage], Flush method [Structured Storage],ILockBytes interface, ILockBytes interface [Structured Storage],Flush method, ILockBytes.Flush, ILockBytes::Flush, _stg_ilockbytes_flush, objidl/ILockBytes::Flush, stg.ilockbytes_flush
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
 - ILockBytes.Flush
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# ILockBytes::Flush


## -description


The 
<b>Flush</b> method ensures that any internal buffers maintained by the 
<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> implementation are written out to the underlying physical storage.


## -parameters






## -returns



This method can return one of these values.




## -remarks



<b>ILockBytes::Flush</b> flushes internal buffers to the underlying storage device.

The COM-provided implementation of compound files calls this method during a transacted commit operation to provide a two-phase commit process that protects against loss of data.




## -see-also




<a href="https://msdn.microsoft.com/700b6a3c-1046-4c21-8887-16f344c23510">ILockBytes - File-Based Implementation</a>



<a href="https://msdn.microsoft.com/6ab019b0-34d7-4b6e-ba77-6b6881fabd29">ILockBytes - Global Memory Implementation</a>



<a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a>
 

 

