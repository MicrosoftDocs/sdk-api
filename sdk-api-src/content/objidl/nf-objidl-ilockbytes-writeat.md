---
UID: NF:objidl.ILockBytes.WriteAt
title: ILockBytes::WriteAt (objidl.h)
description: The WriteAt method writes the specified number of bytes starting at a specified offset from the beginning of the byte array.
helpviewer_keywords: ["ILockBytes interface [Structured Storage]","WriteAt method","ILockBytes.WriteAt","ILockBytes::WriteAt","WriteAt","WriteAt method [Structured Storage]","WriteAt method [Structured Storage]","ILockBytes interface","_stg_ilockbytes_writeat","objidl/ILockBytes::WriteAt","stg.ilockbytes_writeat"]
old-location: stg\ilockbytes_writeat.htm
tech.root: Stg
ms.assetid: a27af4e1-293d-438a-8068-87275a51fd48
ms.date: 12/05/2018
ms.keywords: ILockBytes interface [Structured Storage],WriteAt method, ILockBytes.WriteAt, ILockBytes::WriteAt, WriteAt, WriteAt method [Structured Storage], WriteAt method [Structured Storage],ILockBytes interface, _stg_ilockbytes_writeat, objidl/ILockBytes::WriteAt, stg.ilockbytes_writeat
f1_keywords:
- objidl/ILockBytes.WriteAt
dev_langs:
- c++
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
- ILockBytes.WriteAt
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILockBytes::WriteAt


## -description


The <b>WriteAt</b> method writes the specified number of bytes starting at a specified offset from the beginning of the byte array.


## -parameters




### -param ulOffset [in]

Specifies the starting point from the beginning of the byte array for the data to be written.


### -param pv [in]

Pointer to the buffer containing the data to be written.


### -param cb [in]

Specifies the number of bytes of data to attempt to write into the byte array.


### -param pcbWritten [out]

Pointer to a location where this method specifies the actual number of bytes written to the byte array. You can set this pointer to <b>NULL</b> to indicate that you are not interested in this value. In this case, this method does not provide the actual number of bytes written.


## -returns



This method can return one of these values.




## -remarks



<b>ILockBytes::WriteAt</b> writes the specified data at the specified location in the byte array. The number of bytes actually written must always be returned in <i>pcbWritten</i>, even if an error is returned. If the byte count is zero bytes, the write operation has no effect.

If <i>ulOffset</i> is past the end of the byte array and <i>cb</i> is greater than zero, <b>ILockBytes::WriteAt</b> increases the size of the byte array. The fill bytes written to the byte array are not initialized to any particular value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/ilockbytes-file-based-implementation">ILockBytes - File-Based Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/ilockbytes-global-memory-implementation">ILockBytes - Global Memory Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-readat">ILockBytes::ReadAt</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ilockbytes-setsize">ILockBytes::SetSize</a>
 

 

