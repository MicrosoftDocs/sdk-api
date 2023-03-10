---
UID: NN:wincodec.IWICStream
title: IWICStream (wincodec.h)
description: Represents a Windows Imaging Component (WIC) stream for referencing imaging and metadata content.
helpviewer_keywords: ["IWICStream","IWICStream interface [Windows Imaging Component]","IWICStream interface [Windows Imaging Component]","described","_wic_codec_iwicstream","wic._wic_codec_iwicstream","wincodec/IWICStream"]
old-location: wic\_wic_codec_iwicstream.htm
tech.root: wic
ms.assetid: bc398732-037d-4f48-940f-c70975447972
ms.date: 12/05/2018
ms.keywords: IWICStream, IWICStream interface [Windows Imaging Component], IWICStream interface [Windows Imaging Component],described, _wic_codec_iwicstream, wic._wic_codec_iwicstream, wincodec/IWICStream
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
 - IWICStream
 - wincodec/IWICStream
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
 - IWICStream
---

# IWICStream interface


## -description

Represents a Windows Imaging Component (WIC) stream for referencing imaging and metadata content.

## -inheritance

The <b>IWICStream</b> interface inherits from <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>. <b>IWICStream</b> also has these types of members:

## -remarks

Decoders and metadata handlers are expected to create sub streams of whatever stream they hold when handing off control for embedded metadata to another metadata handler.  If the stream is not restricted then use MAXLONGLONG as the max size and offset 0.

The <b>IWICStream</b> interface methods do not enable you to provide a file sharing option.
            To create a file stream for an image, use the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-shcreatestreamonfileex">SHCreateStreamOnFileEx</a> function.
            This stream can then be used to create an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a> using the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream">CreateDecoderFromStream</a> method.
