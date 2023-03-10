---
UID: NF:mmstream.IMediaStream.GetMultiMediaStream
title: IMediaStream::GetMultiMediaStream (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves a pointer to the multimedia stream that contains the specified media stream.
helpviewer_keywords: ["GetMultiMediaStream","GetMultiMediaStream method [DirectShow]","GetMultiMediaStream method [DirectShow]","IMediaStream interface","IMediaStream interface [DirectShow]","GetMultiMediaStream method","IMediaStream.GetMultiMediaStream","IMediaStream::GetMultiMediaStream","IMediaStreamGetMultiMediaStream","dshow.imediastream_getmultimediastream","mmstream/IMediaStream::GetMultiMediaStream"]
old-location: dshow\imediastream_getmultimediastream.htm
tech.root: dshow
ms.assetid: 09af4bfc-2427-4992-b508-fe9a7ac150d7
ms.date: 12/05/2018
ms.keywords: GetMultiMediaStream, GetMultiMediaStream method [DirectShow], GetMultiMediaStream method [DirectShow],IMediaStream interface, IMediaStream interface [DirectShow],GetMultiMediaStream method, IMediaStream.GetMultiMediaStream, IMediaStream::GetMultiMediaStream, IMediaStreamGetMultiMediaStream, dshow.imediastream_getmultimediastream, mmstream/IMediaStream::GetMultiMediaStream
req.header: mmstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMediaStream::GetMultiMediaStream
 - mmstream/IMediaStream::GetMultiMediaStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmstream.h
api_name:
 - IMediaStream.GetMultiMediaStream
---

# IMediaStream::GetMultiMediaStream


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves a pointer to the multimedia stream that contains the specified media stream.

## -parameters

### -param ppMultiMediaStream [out]

Address of a pointer to an <a href="/windows/desktop/api/mmstream/nn-mmstream-imultimediastream">IMultiMediaStream</a> interface object that will point to the multimedia stream from which the current media stream was created.

## -returns

Returns S_OK if successful or E_POINTER if <i>ppMultiMediaStream</i> is invalid.

## -remarks

This method increments the reference count of the retrieved object pointer.

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream Interface</a>