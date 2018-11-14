---
UID: NF:wincodecsdk.IWICComponentFactory.CreateEncoderPropertyBag
title: IWICComponentFactory::CreateEncoderPropertyBag
author: windows-sdk-content
description: Creates an encoder property bag.
old-location: wic\_wic_codec_iwiccomponentfactory_createencoderpropertybag.htm
tech.root: wic
ms.assetid: 9d3c801d-46d4-4272-8bd6-9bc196e1b187
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CreateEncoderPropertyBag, CreateEncoderPropertyBag method [Windows Imaging Component], CreateEncoderPropertyBag method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateEncoderPropertyBag method, IWICComponentFactory.CreateEncoderPropertyBag, IWICComponentFactory::CreateEncoderPropertyBag, _wic_codec_iwiccomponentfactory_createencoderpropertybag, wic._wic_codec_iwiccomponentfactory_createencoderpropertybag, wincodecsdk/IWICComponentFactory::CreateEncoderPropertyBag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodecsdk.h
: 
- IWICComponentFactory.CreateEncoderPropertyBag
: 
---

# IWICComponentFactory::CreateEncoderPropertyBag


## -description


Creates an encoder property bag.


## -parameters




### -param ppropOptions [in]

Type: <b><a href="_inet_PROPBAG2_Structure_cpp">PROPBAG2</a>*</b>

Pointer to an array of <a href="_inet_PROPBAG2_Structure_cpp">PROPBAG2</a> options used to create the encoder property bag.


### -param cCount [in]

Type: <b>UINT</b>

The number of <a href="_inet_PROPBAG2_Structure_cpp">PROPBAG2</a> structures in the <i>ppropOptions</i> array.


### -param ppIPropertyBag [out]

Type: <b><a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a>**</b>

A pointer that receives a pointer to an encoder <a href="_inet_IPropertyBag2_Interface_cpp">IPropertyBag2</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



