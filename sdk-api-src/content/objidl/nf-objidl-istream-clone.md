---
UID: NF:objidl.IStream.Clone
title: IStream::Clone (objidl.h)
description: The Clone method creates a new stream object with its own seek pointer that references the same bytes as the original stream.
helpviewer_keywords: ["Clone","Clone method [Structured Storage]","Clone method [Structured Storage]","IStream interface","IStream interface [Structured Storage]","Clone method","IStream.Clone","IStream::Clone","_stg_istream_clone","objidl/IStream::Clone","stg.istream_clone"]
old-location: stg\istream_clone.htm
tech.root: Stg
ms.assetid: 677c37fb-598f-4bb0-b5d6-600e0befc722
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Structured Storage], Clone method [Structured Storage],IStream interface, IStream interface [Structured Storage],Clone method, IStream.Clone, IStream::Clone, _stg_istream_clone, objidl/IStream::Clone, stg.istream_clone
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
 - IStream::Clone
 - objidl/IStream::Clone
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
 - IStream.Clone
---

# IStream::Clone


## -description

The <b>Clone</b> method creates a new stream object with its own seek pointer that references the same bytes as the original stream.

## -parameters

### -param ppstm [out]

When successful, pointer to the location of an 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> pointer to the new stream object. If an error occurs, this parameter is <b>NULL</b>.

## -returns

This method can return one of these values.

| Return code | Description |
|----------------|---------------|
|S_OK | The stream was successfully cloned.|
|E_PENDING | Asynchronous Storage only: Part or all of the stream's data is currently unavailable. |
|STG_E_INSUFFICIENTMEMORY | The stream was not cloned due to a lack of memory.|
|STG_E_INVALIDPOINTER | The ppStm pointer is not valid.|
|STG_E_REVERTED | The object has been invalidated by a revert operation above it in the transaction tree.|

## -remarks

The <b>Clone</b> method creates a new stream object for accessing the same bytes but using a separate seek pointer. The new stream object sees the same data as the source-stream object. Changes written to one object are immediately visible in the other. Range locking is shared between the stream objects.

The initial setting of the seek pointer in the cloned stream instance is the same as the current setting of the seek pointer in the original stream at the time of the clone operation.

## -see-also

<a href="/windows/desktop/Stg/istream-compound-file-implementation">IStream - Compound File Implementation</a>



<a href="/windows/desktop/api/objidl/nf-objidl-istream-copyto">IStream::CopyTo</a>