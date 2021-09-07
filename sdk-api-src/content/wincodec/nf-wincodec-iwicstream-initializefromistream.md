---
UID: NF:wincodec.IWICStream.InitializeFromIStream
title: IWICStream::InitializeFromIStream (wincodec.h)
description: Initializes a stream from another stream. Access rights are inherited from the underlying stream.
helpviewer_keywords: ["IWICStream interface [Windows Imaging Component]","InitializeFromIStream method","IWICStream.InitializeFromIStream","IWICStream::InitializeFromIStream","InitializeFromIStream","InitializeFromIStream method [Windows Imaging Component]","InitializeFromIStream method [Windows Imaging Component]","IWICStream interface","_wic_codec_iwicstream_initializefromistream","wic._wic_codec_iwicstream_initializefromistream","wincodec/IWICStream::InitializeFromIStream"]
old-location: wic\_wic_codec_iwicstream_initializefromistream.htm
tech.root: wic
ms.assetid: bfe413e1-f579-4c9c-9e88-3b369235c529
ms.date: 12/05/2018
ms.keywords: IWICStream interface [Windows Imaging Component],InitializeFromIStream method, IWICStream.InitializeFromIStream, IWICStream::InitializeFromIStream, InitializeFromIStream, InitializeFromIStream method [Windows Imaging Component], InitializeFromIStream method [Windows Imaging Component],IWICStream interface, _wic_codec_iwicstream_initializefromistream, wic._wic_codec_iwicstream_initializefromistream, wincodec/IWICStream::InitializeFromIStream
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICStream::InitializeFromIStream
 - wincodec/IWICStream::InitializeFromIStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICStream.InitializeFromIStream
---

# IWICStream::InitializeFromIStream


## -description

Initializes a stream from another stream. Access rights are inherited from the underlying stream.

## -parameters

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The initialize stream.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.