---
UID: NF:wincodec.IWICImagingFactory.CreateComponentEnumerator
title: IWICImagingFactory::CreateComponentEnumerator (wincodec.h)
author: windows-sdk-content
description: Creates an IEnumUnknown object of the specified component types.
old-location: wic\_wic_codec_iwicimagingfactory_createcomponentenumerator.htm
tech.root: wic
ms.assetid: 810bf0c2-2780-4ba3-84c1-7b257139e26e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateComponentEnumerator, CreateComponentEnumerator method [Windows Imaging Component], CreateComponentEnumerator method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateComponentEnumerator method, IWICImagingFactory.CreateComponentEnumerator, IWICImagingFactory::CreateComponentEnumerator, _wic_codec_iwicimagingfactory_createcomponentenumerator, wic._wic_codec_iwicimagingfactory_createcomponentenumerator, wincodec/IWICImagingFactory::CreateComponentEnumerator
ms.topic: method
f1_keywords: ["wincodec/IWICImagingFactory.CreateComponentEnumerator"]
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
 - IWICImagingFactory.CreateComponentEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICImagingFactory::CreateComponentEnumerator


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> object of the specified component types.


## -parameters




### -param componentTypes [in]

Type: <b>DWORD</b>

The types of <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wiccomponenttype">WICComponentType</a> to enumerate.


### -param options [in]

Type: <b>DWORD</b>

The <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ne-wincodec-wiccomponentenumerateoptions">WICComponentEnumerateOptions</a> used to enumerate the given component types. 


### -param ppIEnumUnknown [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>**</b>

A pointer that receives a pointer to a new component enumerator.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Component types must be enumerated seperately. Combinations of component types and <b>WICAllComponents</b> are unsupported.



