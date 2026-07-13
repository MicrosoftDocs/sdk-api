---
UID: NF:wincodec.IWICImagingFactory.CreateComponentInfo
title: IWICImagingFactory::CreateComponentInfo (wincodec.h)
description: Creates a new instance of the IWICComponentInfo class for the given component class identifier (CLSID).
helpviewer_keywords: ["CreateComponentInfo","CreateComponentInfo method [Windows Imaging Component]","CreateComponentInfo method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateComponentInfo method","IWICImagingFactory.CreateComponentInfo","IWICImagingFactory::CreateComponentInfo","_wic_codec_iwicimagingfactory_createcomponentinfo","wic._wic_codec_iwicimagingfactory_createcomponentinfo","wincodec/IWICImagingFactory::CreateComponentInfo"]
old-location: wic\_wic_codec_iwicimagingfactory_createcomponentinfo.htm
tech.root: wic
ms.assetid: c4feebf7-500f-4ab8-85fa-689edfe31846
ms.date: 12/05/2018
ms.keywords: CreateComponentInfo, CreateComponentInfo method [Windows Imaging Component], CreateComponentInfo method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateComponentInfo method, IWICImagingFactory.CreateComponentInfo, IWICImagingFactory::CreateComponentInfo, _wic_codec_iwicimagingfactory_createcomponentinfo, wic._wic_codec_iwicimagingfactory_createcomponentinfo, wincodec/IWICImagingFactory::CreateComponentInfo
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
 - IWICImagingFactory::CreateComponentInfo
 - wincodec/IWICImagingFactory::CreateComponentInfo
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
 - IWICImagingFactory.CreateComponentInfo
---

# IWICImagingFactory::CreateComponentInfo


## -description

Creates a new instance of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccomponentinfo">IWICComponentInfo</a> class for the given component class identifier (CLSID).

## -parameters

### -param clsidComponent [in]

Type: <b>REFCLSID</b>

The CLSID for the desired component.

### -param ppIInfo [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccomponentinfo">IWICComponentInfo</a>**</b>

A pointer that receives a pointer to a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccomponentinfo">IWICComponentInfo</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.