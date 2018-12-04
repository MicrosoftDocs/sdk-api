---
UID: NF:objidl.IFillLockBytes.FillAppend
title: IFillLockBytes::FillAppend
author: windows-sdk-content
description: The FillAppend method writes a new block of bytes to the end of a byte array.
old-location: stg\ifilllockbytes_fillappend.htm
tech.root: stg
ms.assetid: 3f25c48f-85a4-4778-b262-ad0c52cb1ac9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: FillAppend, FillAppend method [Structured Storage], FillAppend method [Structured Storage],IFillLockBytes interface, IFillLockBytes interface [Structured Storage],FillAppend method, IFillLockBytes.FillAppend, IFillLockBytes::FillAppend, _stg_ifilllockbytes_fillappend, objidl/IFillLockBytes::FillAppend, stg.ifilllockbytes_fillappend
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IFillLockBytes.FillAppend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFillLockBytes::FillAppend


## -description


The <b>FillAppend</b> method writes a new block of bytes to the end of a byte array.


## -parameters




### -param pv [in]

Pointer to the data to be appended to the end of an existing byte array. This operation does not create a danger of a memory leak or a buffer overrun.


### -param cb [in]

Size of <i>pv</i> in bytes.


### -param pcbWritten [out]

Number of bytes that were successfully written.


## -returns



This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL.




## -remarks



The 
<b>FillAppend</b> method is used for sequential downloading, where bytes are written to the end of the byte array in the order in which they are received. This method obtains the current size of the byte array (for example, lockbytes object) and writes a new block of data to the end of the array. As each block of data becomes available, the downloader calls this method to write it to the byte array. Subsequent calls by the compound file implementation to 
<a href="https://msdn.microsoft.com/0478d6f0-65c4-445b-946a-692f2373e8f1">ILockBytes::ReadAt</a> return any available data or return E_PENDING if data is currently unavailable.




## -see-also




<a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a>
 

 

