---
UID: NF:propsys.IInitializeWithStream.Initialize
title: IInitializeWithStream::Initialize
author: windows-sdk-content
description: Initializes a handler with a stream.
old-location: shell\IInitializeWithStream_Initialize.htm
tech.root: shell
ms.assetid: 1e04c0a4-aa9b-4e2c-8307-525809ca903f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInitializeWithStream interface [Windows Shell],Initialize method, IInitializeWithStream.Initialize, IInitializeWithStream::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithStream interface, STGM_READ, STGM_READWRITE, propsys/IInitializeWithStream::Initialize, shell.IInitializeWithStream_Initialize, shell_IInitializeWithStream_Initialize
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IInitializeWithStream.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInitializeWithStream::Initialize


## -description


Initializes a handler with a stream.


## -parameters




### -param pstream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface that represents the stream source.


### -param grfMode [in]

Type: <b>DWORD</b>

One of the following <a href="https://msdn.microsoft.com/15a35da9-332a-46e1-9190-500c95e26f59">STGM</a> values that indicates the access mode for <i>pstream</i>.



#### STGM_READ

The stream indicated by <i>pstream</i> is read-only.



#### STGM_READWRITE

The stream indicated by <i>pstream</i> is read/write accessible.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is preferred to <a href="https://msdn.microsoft.com/7b7bb534-dff7-455b-baee-f573fb645cc3">Initialize</a> due to its ability to use streams that are not accessible through a Win32 path, such as the contents of a compressed file with a .zip file name extension.

The stream pointed to by <i>pstream</i> must remain open for the lifetime of the handler or until <a href="https://msdn.microsoft.com/25b6913e-e630-4cae-b155-d9d475593c9e">IPropertyStore::Commit</a> is called.

When first opened, the source stream reference points to the beginning of the stream. The handler can seek and read from the stream at any time. A handler can be implemented to read all properties from the stream during <b>Initialize</b> or it can wait until the calling process attempts to enumerate or read properties before fetching them from the stream.

A handler instance should be initialized only once in its lifetime. Attempts by the caller to reinitialize the handler should result in the error <code>HRESULT_FROM_WIN32(ERROR_ALREADY_INITIALIZED)</code>.



