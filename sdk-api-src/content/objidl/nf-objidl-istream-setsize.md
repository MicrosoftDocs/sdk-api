---
UID: NF:objidl.IStream.SetSize
title: IStream::SetSize (objidl.h)
description: Changes the size of the stream object.
helpviewer_keywords: ["IStream interface [Structured Storage]","SetSize method","IStream.SetSize","IStream::SetSize","SetSize","SetSize method [Structured Storage]","SetSize method [Structured Storage]","IStream interface","_stg_istream_setsize","objidl/IStream::SetSize","stg.istream_setsize"]
old-location: stg\istream_setsize.htm
tech.root: Stg
ms.assetid: 05627db5-067b-4a1a-a7ed-c83314f8bd8d
ms.date: 12/05/2018
ms.keywords: IStream interface [Structured Storage],SetSize method, IStream.SetSize, IStream::SetSize, SetSize, SetSize method [Structured Storage], SetSize method [Structured Storage],IStream interface, _stg_istream_setsize, objidl/IStream::SetSize, stg.istream_setsize
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
 - IStream::SetSize
 - objidl/IStream::SetSize
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
 - IStream.SetSize
---

# IStream::SetSize


## -description

The <b>SetSize</b> method changes the size of the stream object.

## -parameters

### -param libNewSize [in]

Specifies the new size, in bytes, of the stream.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The size of the stream object was successfully changed.|
|E_PENDING | Asynchronous Storage only: Part or all of the stream's data is currently unavailable.|
|STG_E_MEDIUMFULL | The stream size is not changed because there is no space left on the storage device.|
|STG_E_INVALIDFUNCTION | The value of the *libNewSize* parameter is not supported by the implementation. Not all streams support greater than 232 bytes. If a stream does not support more than 232 bytes, the high DWORD data type of *libNewSize* must be zero. If it is nonzero, the implementation may return STG_E_INVALIDFUNCTION. In general, COM-based implementations of the IStream interface do not support streams larger than 232 bytes.|
|STG_E_REVERTED | The object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

<b>IStream::SetSize</b> changes the size of the stream object. Call this method to preallocate space for the stream. If the <i>libNewSize</i> parameter is larger than the current stream size, the stream is extended to the indicated size by filling the intervening space with bytes of undefined value. This operation is similar to the 
<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> method if the seek pointer is past the current end of the stream.

If the <i>libNewSize</i> parameter is smaller than the current stream, the stream is truncated to the indicated size.

The seek pointer is not affected by the change in stream size.

Calling <b>IStream::SetSize</b> can be an effective way to obtain a large chunk of contiguous space.

## -see-also

<a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>



<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>