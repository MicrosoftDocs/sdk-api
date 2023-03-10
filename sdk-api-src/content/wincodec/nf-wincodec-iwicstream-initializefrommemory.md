---
UID: NF:wincodec.IWICStream.InitializeFromMemory
title: IWICStream::InitializeFromMemory (wincodec.h)
description: Initializes a stream to treat a block of memory as a stream. The stream cannot grow beyond the buffer size.
helpviewer_keywords: ["IWICStream interface [Windows Imaging Component]","InitializeFromMemory method","IWICStream.InitializeFromMemory","IWICStream::InitializeFromMemory","InitializeFromMemory","InitializeFromMemory method [Windows Imaging Component]","InitializeFromMemory method [Windows Imaging Component]","IWICStream interface","_wic_codec_iwicstream_initializefrommemory","wic._wic_codec_iwicstream_initializefrommemory","wincodec/IWICStream::InitializeFromMemory"]
old-location: wic\_wic_codec_iwicstream_initializefrommemory.htm
tech.root: wic
ms.assetid: 7e226759-61aa-4f06-b20f-d5853faf4e4b
ms.date: 12/05/2018
ms.keywords: IWICStream interface [Windows Imaging Component],InitializeFromMemory method, IWICStream.InitializeFromMemory, IWICStream::InitializeFromMemory, InitializeFromMemory, InitializeFromMemory method [Windows Imaging Component], InitializeFromMemory method [Windows Imaging Component],IWICStream interface, _wic_codec_iwicstream_initializefrommemory, wic._wic_codec_iwicstream_initializefrommemory, wincodec/IWICStream::InitializeFromMemory
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
 - IWICStream::InitializeFromMemory
 - wincodec/IWICStream::InitializeFromMemory
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
 - IWICStream.InitializeFromMemory
---

# IWICStream::InitializeFromMemory


## -description

Initializes a stream to treat a block of memory as a stream. The stream cannot grow beyond the buffer size.

## -parameters

### -param pbBuffer [in]

Type: <b>BYTE*</b>

Pointer to the buffer used to initialize the stream.

### -param cbBufferSize [in]

Type: <b>DWORD</b>

The size of buffer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method should be avoided whenever possible. The caller is responsible for ensuring the memory block is valid for the lifetime of the stream when using <b>InitializeFromMemory</b>.  A workaround for this behavior is to create an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> and use <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicstream-initializefromistream">InitializeFromIStream</a> to create the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicstream">IWICStream</a>.

If you require a growable memory stream, use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal">CreateStreamOnHGlobal</a>.