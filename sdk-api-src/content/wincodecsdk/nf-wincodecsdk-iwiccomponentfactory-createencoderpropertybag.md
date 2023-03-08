---
UID: NF:wincodecsdk.IWICComponentFactory.CreateEncoderPropertyBag
title: IWICComponentFactory::CreateEncoderPropertyBag (wincodecsdk.h)
description: Creates an encoder property bag.
helpviewer_keywords: ["CreateEncoderPropertyBag","CreateEncoderPropertyBag method [Windows Imaging Component]","CreateEncoderPropertyBag method [Windows Imaging Component]","IWICComponentFactory interface","IWICComponentFactory interface [Windows Imaging Component]","CreateEncoderPropertyBag method","IWICComponentFactory.CreateEncoderPropertyBag","IWICComponentFactory::CreateEncoderPropertyBag","_wic_codec_iwiccomponentfactory_createencoderpropertybag","wic._wic_codec_iwiccomponentfactory_createencoderpropertybag","wincodecsdk/IWICComponentFactory::CreateEncoderPropertyBag"]
old-location: wic\_wic_codec_iwiccomponentfactory_createencoderpropertybag.htm
tech.root: wic
ms.assetid: 9d3c801d-46d4-4272-8bd6-9bc196e1b187
ms.date: 12/05/2018
ms.keywords: CreateEncoderPropertyBag, CreateEncoderPropertyBag method [Windows Imaging Component], CreateEncoderPropertyBag method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateEncoderPropertyBag method, IWICComponentFactory.CreateEncoderPropertyBag, IWICComponentFactory::CreateEncoderPropertyBag, _wic_codec_iwiccomponentfactory_createencoderpropertybag, wic._wic_codec_iwiccomponentfactory_createencoderpropertybag, wincodecsdk/IWICComponentFactory::CreateEncoderPropertyBag
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICComponentFactory::CreateEncoderPropertyBag
 - wincodecsdk/IWICComponentFactory::CreateEncoderPropertyBag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICComponentFactory.CreateEncoderPropertyBag
---

# IWICComponentFactory::CreateEncoderPropertyBag


## -description

Creates an encoder property bag.

## -parameters

### -param ppropOptions [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)">PROPBAG2</a>*</b>

Pointer to an array of <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)">PROPBAG2</a> options used to create the encoder property bag.

### -param cCount [in]

Type: <b>UINT</b>

The number of <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768188(v=vs.85)">PROPBAG2</a> structures in the <i>ppropOptions</i> array.

### -param ppIPropertyBag [out]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a>**</b>

A pointer that receives a pointer to an encoder <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)">IPropertyBag2</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.