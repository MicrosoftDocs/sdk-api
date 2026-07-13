---
UID: NF:propsys.IInitializeWithStream.Initialize
title: IInitializeWithStream::Initialize (propsys.h)
description: Initializes a handler with a stream.
helpviewer_keywords: ["IInitializeWithStream interface [Windows Shell]","Initialize method","IInitializeWithStream.Initialize","IInitializeWithStream::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IInitializeWithStream interface","STGM_READ","STGM_READWRITE","propsys/IInitializeWithStream::Initialize","shell.IInitializeWithStream_Initialize","shell_IInitializeWithStream_Initialize"]
old-location: shell\IInitializeWithStream_Initialize.htm
tech.root: shell
ms.assetid: 1e04c0a4-aa9b-4e2c-8307-525809ca903f
ms.date: 12/05/2018
ms.keywords: IInitializeWithStream interface [Windows Shell],Initialize method, IInitializeWithStream.Initialize, IInitializeWithStream::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithStream interface, STGM_READ, STGM_READWRITE, propsys/IInitializeWithStream::Initialize, shell.IInitializeWithStream_Initialize, shell_IInitializeWithStream_Initialize
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInitializeWithStream::Initialize
 - propsys/IInitializeWithStream::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IInitializeWithStream.Initialize
---

# IInitializeWithStream::Initialize


## -description

Initializes a handler with a stream.

## -parameters

### -param pstream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface that represents the stream source.

### -param grfMode [in]

Type: <b>DWORD</b>

One of the following <a href="/windows/desktop/Stg/stgm-constants">STGM</a> values that indicates the access mode for <i>pstream</i>.



#### STGM_READ

The stream indicated by <i>pstream</i> is read-only.



#### STGM_READWRITE

The stream indicated by <i>pstream</i> is read/write accessible.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is preferred to <a href="/windows/desktop/api/propsys/nf-propsys-iinitializewithfile-initialize">Initialize</a> due to its ability to use streams that are not accessible through a Win32 path, such as the contents of a compressed file with a .zip file name extension.

The stream pointed to by <i>pstream</i> must remain open for the lifetime of the handler or until <a href="/previous-versions/windows/desktop/legacy/bb761470(v=vs.85)">IPropertyStore::Commit</a> is called.

When first opened, the source stream reference points to the beginning of the stream. The handler can seek and read from the stream at any time. A handler can be implemented to read all properties from the stream during <b>Initialize</b> or it can wait until the calling process attempts to enumerate or read properties before fetching them from the stream.

A handler instance should be initialized only once in its lifetime. Attempts by the caller to reinitialize the handler should result in the error <code>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</code>.