---
UID: NF:objidl.ILockBytes.ReadAt
title: ILockBytes::ReadAt (objidl.h)
description: The ReadAt method reads a specified number of bytes starting at a specified offset from the beginning of the byte array object.
helpviewer_keywords: ["ILockBytes interface [Structured Storage]","ReadAt method","ILockBytes.ReadAt","ILockBytes::ReadAt","ReadAt","ReadAt method [Structured Storage]","ReadAt method [Structured Storage]","ILockBytes interface","_stg_ilockbytes_readat","objidl/ILockBytes::ReadAt","stg.ilockbytes_readat"]
old-location: stg\ilockbytes_readat.htm
tech.root: Stg
ms.assetid: 0478d6f0-65c4-445b-946a-692f2373e8f1
ms.date: 12/05/2018
ms.keywords: ILockBytes interface [Structured Storage],ReadAt method, ILockBytes.ReadAt, ILockBytes::ReadAt, ReadAt, ReadAt method [Structured Storage], ReadAt method [Structured Storage],ILockBytes interface, _stg_ilockbytes_readat, objidl/ILockBytes::ReadAt, stg.ilockbytes_readat
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILockBytes::ReadAt
 - objidl/ILockBytes::ReadAt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ILockBytes.ReadAt
---

# ILockBytes::ReadAt


## -description

The <b>ReadAt</b> method reads a specified number of bytes starting at a specified offset from the beginning of the byte array object.

## -parameters

### -param ulOffset [in]

Specifies the starting point from the beginning of the byte array for reading data.

### -param pv [in]

Pointer to the buffer into which the byte array is read.  The size of this buffer is contained in <i>cb</i>.

### -param cb [in]

Specifies the number of bytes of data to attempt to read from the byte array.

### -param pcbRead [out]

Pointer to a <b>ULONG</b> where this method writes the actual number of bytes read from the byte array. You can set this pointer to <b>NULL</b> to indicate that you are not interested in this value. In this case, this method does not provide the actual number of bytes that were read.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | Indicates that the specified number of bytes were read, or the maximum number of bytes were read to the end of the byte array.|
|E_FAIL | Data could not be read from the byte array.|
|E_PENDING | Asynchronous Storage only: Part or all of the data to be read is currently unavailable. |
|STG_E_ACCESSDENIED | The caller does not have permission to access the byte array.|
|STG_E_READFAULT | The number of bytes to be read does not equal the number of bytes that were actually read.|

## -remarks

<b>ILockBytes::ReadAt</b> reads bytes from the byte array object. It reports the number of bytes that were actually read. This value may be less than the number of bytes requested if an error occurs or if the end of the byte array is reached during the read.

It is not an error to read less than the specified number of bytes if the operation encounters the end of the byte array. Note that this is the same end-of-file behavior as found in MS-DOS file allocation table (FAT) file system files.

## -see-also

<a href="/windows/desktop/Stg/ilockbytes-file-based-implementation">ILockBytes - File-Based Implementation</a>



<a href="/windows/desktop/Stg/ilockbytes-global-memory-implementation">ILockBytes - Global Memory Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-ilockbytes-writeat">ILockBytes::WriteAt</a>