---
UID: NF:wincodecsdk.IWICPersistStream.LoadEx
title: IWICPersistStream::LoadEx (wincodecsdk.h)
description: Loads data from an input stream using the given parameters.
helpviewer_keywords: ["IWICPersistStream interface [Windows Imaging Component]","LoadEx method","IWICPersistStream.LoadEx","IWICPersistStream::LoadEx","LoadEx","LoadEx method [Windows Imaging Component]","LoadEx method [Windows Imaging Component]","IWICPersistStream interface","_wic_codec_iwicpersiststream_loadex","wic._wic_codec_iwicpersiststream_loadex","wincodecsdk/IWICPersistStream::LoadEx"]
old-location: wic\_wic_codec_iwicpersiststream_loadex.htm
tech.root: wic
ms.assetid: cb200a21-6c01-469e-b70f-f787f1dae382
ms.date: 12/05/2018
ms.keywords: IWICPersistStream interface [Windows Imaging Component],LoadEx method, IWICPersistStream.LoadEx, IWICPersistStream::LoadEx, LoadEx, LoadEx method [Windows Imaging Component], LoadEx method [Windows Imaging Component],IWICPersistStream interface, _wic_codec_iwicpersiststream_loadex, wic._wic_codec_iwicpersiststream_loadex, wincodecsdk/IWICPersistStream::LoadEx
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
 - IWICPersistStream::LoadEx
 - wincodecsdk/IWICPersistStream::LoadEx
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
 - IWICPersistStream.LoadEx
---

# IWICPersistStream::LoadEx


## -description

Loads data from an input stream using the given parameters.

## -parameters

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to the input stream.

### -param pguidPreferredVendor [in]

Type: <b>const GUID*</b>

Pointer to the GUID of the preferred vendor .

### -param dwPersistOptions [in]

Type: <b>DWORD</b>

The <a href="/windows/desktop/api/wincodecsdk/ne-wincodecsdk-wicpersistoptions">WICPersistOptions</a> used to load the stream.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

NULL can be passed in for <i>pguidPreferredVendor</i> to indicate no preference.