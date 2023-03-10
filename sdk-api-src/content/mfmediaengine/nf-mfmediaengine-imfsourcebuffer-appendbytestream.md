---
UID: NF:mfmediaengine.IMFSourceBuffer.AppendByteStream
title: IMFSourceBuffer::AppendByteStream (mfmediaengine.h)
description: Appends the media segment from the specified byte stream to the IMFSourceBuffer.
helpviewer_keywords: ["AppendByteStream","AppendByteStream method [Media Foundation]","AppendByteStream method [Media Foundation]","IMFSourceBuffer interface","IMFSourceBuffer interface [Media Foundation]","AppendByteStream method","IMFSourceBuffer.AppendByteStream","IMFSourceBuffer::AppendByteStream","mf.imfsourcebuffer_appendbytestream","mfmediaengine/IMFSourceBuffer::AppendByteStream"]
old-location: mf\imfsourcebuffer_appendbytestream.htm
tech.root: mf
ms.assetid: 1a4fc611-4923-48ad-bc92-c3686d855c13
ms.date: 12/05/2018
ms.keywords: AppendByteStream, AppendByteStream method [Media Foundation], AppendByteStream method [Media Foundation],IMFSourceBuffer interface, IMFSourceBuffer interface [Media Foundation],AppendByteStream method, IMFSourceBuffer.AppendByteStream, IMFSourceBuffer::AppendByteStream, mf.imfsourcebuffer_appendbytestream, mfmediaengine/IMFSourceBuffer::AppendByteStream
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFSourceBuffer::AppendByteStream
 - mfmediaengine/IMFSourceBuffer::AppendByteStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFSourceBuffer.AppendByteStream
---

# IMFSourceBuffer::AppendByteStream


## -description

Appends the media segment from the specified byte stream to the <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a>.

## -parameters

### -param pStream [in]

The media segment data.

### -param pMaxLen [in]

The maximum length of the media segment data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a>