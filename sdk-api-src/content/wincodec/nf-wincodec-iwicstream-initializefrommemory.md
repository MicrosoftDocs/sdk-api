---
UID: NF:wincodec.IWICStream.InitializeFromMemory
title: IWICStream::InitializeFromMemory
author: windows-sdk-content
description: Initializes a stream to treat a block of memory as a stream. The stream cannot grow beyond the buffer size.
old-location: wic\_wic_codec_iwicstream_initializefrommemory.htm
tech.root: wic
ms.assetid: 7e226759-61aa-4f06-b20f-d5853faf4e4b
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICStream interface [Windows Imaging Component],InitializeFromMemory method, IWICStream.InitializeFromMemory, IWICStream::InitializeFromMemory, InitializeFromMemory, InitializeFromMemory method [Windows Imaging Component], InitializeFromMemory method [Windows Imaging Component],IWICStream interface, _wic_codec_iwicstream_initializefrommemory, wic._wic_codec_iwicstream_initializefrommemory, wincodec/IWICStream::InitializeFromMemory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICStream.InitializeFromMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodec.h
: 
- IWICStream.InitializeFromMemory
: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method should be avoided whenever possible. The caller is responsible for ensuring the memory block is valid for the lifetime of the stream when using <b>InitializeFromMemory</b>.  A workaround for this behavior is to create an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> and use <a href="https://msdn.microsoft.com/bfe413e1-f579-4c9c-9e88-3b369235c529">InitializeFromIStream</a> to create the <a href="https://msdn.microsoft.com/bc398732-037d-4f48-940f-c70975447972">IWICStream</a>.

If you require a growable memory stream, use <a href="https://msdn.microsoft.com/413c107b-a943-4c02-9c00-aea708e876d7">CreateStreamOnHGlobal</a>.



