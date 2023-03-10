---
UID: NF:objidl.IStream.Seek
title: IStream::Seek (objidl.h)
description: Changes the seek pointer to a new location. The new location is relative to either the beginning of the stream, the end of the stream, or the current seek pointer.
helpviewer_keywords: ["IStream interface [Structured Storage]","Seek method","IStream.Seek","IStream::Seek","Seek","Seek method [Structured Storage]","Seek method [Structured Storage]","IStream interface","_stg_istream_seek","objidl/IStream::Seek","stg.istream_seek"]
old-location: stg\istream_seek.htm
tech.root: Stg
ms.assetid: ea087c6d-8854-4a81-b37b-15ab76630973
ms.date: 12/05/2018
ms.keywords: IStream interface [Structured Storage],Seek method, IStream.Seek, IStream::Seek, Seek, Seek method [Structured Storage], Seek method [Structured Storage],IStream interface, _stg_istream_seek, objidl/IStream::Seek, stg.istream_seek
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
 - IStream::Seek
 - objidl/IStream::Seek
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
 - IStream.Seek
---

# IStream::Seek


## -description

The <b>Seek</b> method changes the seek pointer to a new location.  The new location is relative to either the beginning of the stream, the end of the stream, or the current seek pointer.

## -parameters

### -param dlibMove [in]

The displacement to be added to the location indicated by the <i>dwOrigin</i> parameter. If <i>dwOrigin</i> is <b>STREAM_SEEK_SET</b>, this is interpreted as an unsigned value rather than a signed value.

### -param dwOrigin [in]

The origin for the displacement specified in <i>dlibMove</i>. The origin can be the beginning of the file (<b>STREAM_SEEK_SET</b>), the current seek pointer (<b>STREAM_SEEK_CUR</b>), or the end of the file (<b>STREAM_SEEK_END</b>). For more information about values, see the <a href="/windows/desktop/api/objidl/ne-objidl-stream_seek">STREAM_SEEK</a> enumeration.

### -param plibNewPosition [out]

A pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream. 

You can set this pointer to <b>NULL</b>. In this case, this method does not provide the new seek pointer.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The seek pointer was successfully adjusted.|
|E_PENDING | Asynchronous Storage only: Part or all of the stream data is currently unavailable. |
|STG_E_INVALIDPOINTER | Indicates that *plibNewPosition* points to invalid memory, because *plibNewPosition* is not read.|
|STG_E_INVALIDFUNCTION | The *dwOrigin* parameter contains an invalid value, or the *dlibMove* parameter contains a bad offset value. For example, the result of the seek pointer is a negative offset value.|
|STG_E_REVERTED | The object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

<b>IStream::Seek</b> changes the seek pointer so that subsequent read and write operations can be performed at a different location in the stream object. It is an error to seek before the beginning of the stream. It is not, however, an error to seek past the end of the stream. Seeking past the end of the stream is useful for subsequent write operations, as the stream byte range will be extended to the new seek position immediately before the write is complete.

You can also use this method to obtain the current value of the seek pointer by calling this method with the <i>dwOrigin</i> parameter set to <b>STREAM_SEEK_CUR</b> and the <i>dlibMove</i> parameter set to 0 so that the seek pointer is not changed. The current seek pointer is returned in the <i>plibNewPosition</i> parameter.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a>



<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a>



<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/ne-objidl-stream_seek">STREAM_SEEK</a>