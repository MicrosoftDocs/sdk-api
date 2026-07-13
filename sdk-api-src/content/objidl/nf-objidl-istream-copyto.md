---
UID: NF:objidl.IStream.CopyTo
title: IStream::CopyTo (objidl.h)
description: Copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.
helpviewer_keywords: ["CopyTo","CopyTo method [Structured Storage]","CopyTo method [Structured Storage]","IStream interface","IStream interface [Structured Storage]","CopyTo method","IStream.CopyTo","IStream::CopyTo","_stg_istream_copyto","objidl/IStream::CopyTo","stg.istream_copyto"]
old-location: stg\istream_copyto.htm
tech.root: Stg
ms.assetid: 5bcd7da6-8bd5-4ab7-952f-f0a12e87f2d4
ms.date: 12/05/2018
ms.keywords: CopyTo, CopyTo method [Structured Storage], CopyTo method [Structured Storage],IStream interface, IStream interface [Structured Storage],CopyTo method, IStream.CopyTo, IStream::CopyTo, _stg_istream_copyto, objidl/IStream::CopyTo, stg.istream_copyto
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
 - IStream::CopyTo
 - objidl/IStream::CopyTo
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
 - IStream.CopyTo
---

# IStream::CopyTo


## -description

The <b>CopyTo</b> method copies a specified number of bytes from the current seek pointer in the stream to the current seek pointer in another stream.

## -parameters

### -param pstm [in]

A pointer to the destination stream. The stream pointed to by <i>pstm</i> can be a new stream or a clone of the source stream.

### -param cb [in]

The number of bytes to copy from the source stream.

### -param pcbRead [out]

A pointer to the location where this method writes the actual number of bytes read from the source. You can set this pointer to <b>NULL</b>. In this case, this method does not provide the actual number of bytes read.

### -param pcbWritten [out]

A pointer to the location where this method writes the actual number of bytes written to the destination. You can set this pointer to <b>NULL</b>. In this case, this method does not provide the actual number of bytes written.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The stream object was successfully copied.|
|E_PENDING | Asynchronous Storage only: Part or all of the data to be copied is currently unavailable. |
|STG_E_INVALIDPOINTER | The value of one of the pointer parameters is invalid.|
|STG_E_MEDIUMFULL | The stream is not copied because there is no space left on the storage device.|
|STG_E_REVERTED | The object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

The <b>CopyTo</b> method copies the specified bytes from one stream to another. It can also be used to copy a stream to itself. The seek pointer in each stream instance is adjusted for the number of bytes read or written. This method is equivalent to reading <i>cb</i> bytes into memory using 
<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> and then immediately writing them to the destination stream using 
<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a>, although <b>IStream::CopyTo</b> will be more efficient.

The destination stream can be a clone of the source stream created by calling the 
<a href="/windows/desktop/api/objidl/nf-objidl-istream-clone">IStream::Clone</a> method.

If <b>IStream::CopyTo</b> returns an error, you cannot assume that the seek pointers are valid for either the source or destination. Additionally, the values of <i>pcbRead</i> and <i>pcbWritten</i> are not meaningful even though they are returned.

If <b>IStream::CopyTo</b> returns successfully, the actual number of bytes read and written are the same.

To copy the remainder of the source from the current seek pointer, specify the maximum large integer value for the <i>cb</i> parameter. If the seek pointer is the beginning of the stream, this operation copies the entire stream.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a>



<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a>



<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istream-clone">IStream::Clone</a>