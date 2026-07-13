---
UID: NF:mfreadwrite.IMFSinkWriter.AddStream
title: IMFSinkWriter::AddStream (mfreadwrite.h)
description: Adds a stream to the sink writer.
helpviewer_keywords: ["AddStream","AddStream method [Media Foundation]","AddStream method [Media Foundation]","IMFSinkWriter interface","IMFSinkWriter interface [Media Foundation]","AddStream method","IMFSinkWriter.AddStream","IMFSinkWriter::AddStream","mf.imfsinkwriter_addstream","mfreadwrite/IMFSinkWriter::AddStream"]
old-location: mf\imfsinkwriter_addstream.htm
tech.root: mf
ms.assetid: 9f9b1216-e915-4188-bcfd-6c41e1821ec4
ms.date: 12/05/2018
ms.keywords: AddStream, AddStream method [Media Foundation], AddStream method [Media Foundation],IMFSinkWriter interface, IMFSinkWriter interface [Media Foundation],AddStream method, IMFSinkWriter.AddStream, IMFSinkWriter::AddStream, mf.imfsinkwriter_addstream, mfreadwrite/IMFSinkWriter::AddStream
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFSinkWriter::AddStream
 - mfreadwrite/IMFSinkWriter::AddStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfreadwrite.h
api_name:
 - IMFSinkWriter.AddStream
---

# IMFSinkWriter::AddStream


## -description

Adds a stream to the sink writer.

## -parameters

### -param pTargetMediaType [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of a media type. This media type specifies the format of the samples that will be written to the file. It does not need to match the input format. To set the input format, call <a href="/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype">IMFSinkWriter::SetInputMediaType</a>.

### -param pdwStreamIndex [out]

Receives the zero-based index of the new stream.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.

## -see-also

<a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="/windows/desktop/medfound/sink-writer">Sink Writer</a>