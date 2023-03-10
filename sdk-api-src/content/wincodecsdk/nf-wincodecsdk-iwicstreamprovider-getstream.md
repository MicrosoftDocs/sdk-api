---
UID: NF:wincodecsdk.IWICStreamProvider.GetStream
title: IWICStreamProvider::GetStream (wincodecsdk.h)
description: Gets the stream held by the component.
helpviewer_keywords: ["GetStream","GetStream method [Windows Imaging Component]","GetStream method [Windows Imaging Component]","IWICStreamProvider interface","IWICStreamProvider interface [Windows Imaging Component]","GetStream method","IWICStreamProvider.GetStream","IWICStreamProvider::GetStream","_wic_codec_iwicstreamprovider_getstream","wic._wic_codec_iwicstreamprovider_getstream","wincodecsdk/IWICStreamProvider::GetStream"]
old-location: wic\_wic_codec_iwicstreamprovider_getstream.htm
tech.root: wic
ms.assetid: c86e507b-0b1d-4de0-8af5-c46d7870fb09
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [Windows Imaging Component], GetStream method [Windows Imaging Component],IWICStreamProvider interface, IWICStreamProvider interface [Windows Imaging Component],GetStream method, IWICStreamProvider.GetStream, IWICStreamProvider::GetStream, _wic_codec_iwicstreamprovider_getstream, wic._wic_codec_iwicstreamprovider_getstream, wincodecsdk/IWICStreamProvider::GetStream
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
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
 - IWICStreamProvider::GetStream
 - wincodecsdk/IWICStreamProvider::GetStream
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
 - IWICStreamProvider.GetStream
---

# IWICStreamProvider::GetStream


## -description

Gets the stream held by the component.

## -parameters

### -param ppIStream [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>**</b>

Pointer that receives a pointer to the stream held by the component.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.