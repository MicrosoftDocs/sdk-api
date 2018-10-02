---
UID: NF:wincodec.IWICStream.InitializeFromIStreamRegion
title: IWICStream::InitializeFromIStreamRegion
author: windows-sdk-content
description: Initializes the stream as a substream of another stream.
old-location: wic\_wic_codec_iwicstream_initializefromistreamregion.htm
tech.root: wic
ms.assetid: 508e1972-22ef-4211-adcf-03f8138624c9
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWICStream interface [Windows Imaging Component],InitializeFromIStreamRegion method, IWICStream.InitializeFromIStreamRegion, IWICStream::InitializeFromIStreamRegion, InitializeFromIStreamRegion, InitializeFromIStreamRegion method [Windows Imaging Component], InitializeFromIStreamRegion method [Windows Imaging Component],IWICStream interface, _wic_codec_iwicstream_initializefromistreamregion, wic._wic_codec_iwicstream_initializefromistreamregion, wincodec/IWICStream::InitializeFromIStreamRegion
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
 - IWICStream.InitializeFromIStreamRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICStream::InitializeFromIStreamRegion


## -description


Initializes the stream as a substream of another stream.


## -parameters




### -param pIStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

Pointer to the input stream.


### -param ulOffset [in]

Type: <b>ULARGE_INTEGER</b>

The stream offset used to create the new stream.


### -param ulMaxSize [in]

Type: <b>ULARGE_INTEGER</b>

The maximum size of the stream.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The stream functions with its own stream position, independent of the underlying stream but restricted to a region.  All seek positions are relative to the sub region.  It is allowed, though not recommended, to have multiple writable sub streams overlapping the same range.



