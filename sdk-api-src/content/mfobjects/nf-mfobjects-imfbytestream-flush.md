---
UID: NF:mfobjects.IMFByteStream.Flush
title: IMFByteStream::Flush (mfobjects.h)
description: Clears any internal buffers used by the stream. If you are writing to the stream, the buffered data is written to the underlying file or device.
helpviewer_keywords: ["16ea6c38-52f3-405e-8a8f-be5d0527099c","Flush","Flush method [Media Foundation]","Flush method [Media Foundation]","IMFByteStream interface","IMFByteStream interface [Media Foundation]","Flush method","IMFByteStream.Flush","IMFByteStream::Flush","mf.imfbytestream_flush","mfobjects/IMFByteStream::Flush"]
old-location: mf\imfbytestream_flush.htm
tech.root: mf
ms.assetid: 16ea6c38-52f3-405e-8a8f-be5d0527099c
ms.date: 12/05/2018
ms.keywords: 16ea6c38-52f3-405e-8a8f-be5d0527099c, Flush, Flush method [Media Foundation], Flush method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],Flush method, IMFByteStream.Flush, IMFByteStream::Flush, mf.imfbytestream_flush, mfobjects/IMFByteStream::Flush
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStream::Flush
 - mfobjects/IMFByteStream::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStream.Flush
---

# IMFByteStream::Flush


## -description

Clears any internal buffers used by the stream. If you are writing to the stream, the buffered data is written to the underlying file or device.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the byte stream is read-only, this method has no effect.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>
