---
UID: NF:objidl.ISequentialStream.Read
title: ISequentialStream::Read (objidl.h)
description: Reads a specified number of bytes from the stream object into memory, starting at the current seek pointer.
helpviewer_keywords: ["ISequentialStream interface [Structured Storage]","Read method","ISequentialStream.Read","ISequentialStream::Read","Read","Read method [Structured Storage]","Read method [Structured Storage]","ISequentialStream interface","_stg_isequentialstream_read","objidl/ISequentialStream::Read","stg.isequentialstream_read"]
old-location: stg\isequentialstream_read.htm
tech.root: Stg
ms.assetid: 934a90bb-5ed0-4d80-9906-352ad8586655
ms.date: 12/05/2018
ms.keywords: ISequentialStream interface [Structured Storage],Read method, ISequentialStream.Read, ISequentialStream::Read, Read, Read method [Structured Storage], Read method [Structured Storage],ISequentialStream interface, _stg_isequentialstream_read, objidl/ISequentialStream::Read, stg.isequentialstream_read
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
 - ISequentialStream::Read
 - objidl/ISequentialStream::Read
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
 - ISequentialStream.Read
---

# ISequentialStream::Read


## -description

The <b>Read</b> method reads a specified number of bytes from the stream object into memory, starting at the current seek pointer.

## -parameters

### -param pv [out]

A pointer to the buffer which the stream data is read into.

### -param cb [in]

The number of bytes of data to read from the stream object.

### -param pcbRead [out]

A pointer to a <b>ULONG</b> variable that receives the actual number of bytes read from the stream object. 

<div class="alert"><b>Note</b>  The number of bytes read may be zero.</div>
<div> </div>

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | All of the requested data was successfully read from the stream object; the number of bytes requested in *cb* is the same as the number of bytes returned in *pcbRead*.|
|S_FALSE | The value returned in *pcbRead* is less than the number of bytes requested in *cb*. This indicates the end of the stream has been reached. The number of bytes read indicates how much of the *pv* buffer has been filled.|
|E_PENDING | Asynchronous storage only: Part or all of the data to be read is currently unavailable. |
|STG_E_ACCESSDENIED | The caller does not have permissions required to read this stream object.|
|STG_E_INVALIDPOINTER | One of the pointer values is invalid.|
|STG_E_REVERTED | The object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

This method reads bytes from this stream object into memory. The stream object must be opened in <b>STGM_READ</b> mode. This method adjusts the seek pointer by the actual number of bytes read.

The number of bytes actually read is also returned in the <i>pcbRead</i> parameter.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The actual number of bytes read can be less than the number of bytes requested if an error occurs or if the end of the stream is reached during the read operation.  The number of bytes returned should always  be compared to the number of bytes requested.  If the number of bytes returned is less than the number of bytes requested, it usually means the <b>Read</b> method attempted to read  past the end of the stream.

The application should handle both a returned error  and <b>S_OK</b> return values on end-of-stream read operations.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istorage-openstream">IStorage::OpenStream</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>



<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="/windows/desktop/api/wtypes/ne-wtypes-stgmove">STGMOVE</a>