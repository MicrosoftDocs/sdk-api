---
UID: NF:wincodec.IWICImagingFactory.CreateComponentEnumerator
title: IWICImagingFactory::CreateComponentEnumerator
author: windows-sdk-content
description: Creates an IEnumUnknown object of the specified component types.
old-location: wic\_wic_codec_iwicimagingfactory_createcomponentenumerator.htm
tech.root: wic
ms.assetid: 810bf0c2-2780-4ba3-84c1-7b257139e26e
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateComponentEnumerator, CreateComponentEnumerator method [Windows Imaging Component], CreateComponentEnumerator method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateComponentEnumerator method, IWICImagingFactory.CreateComponentEnumerator, IWICImagingFactory::CreateComponentEnumerator, _wic_codec_iwicimagingfactory_createcomponentenumerator, wic._wic_codec_iwicimagingfactory_createcomponentenumerator, wincodec/IWICImagingFactory::CreateComponentEnumerator
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
 - IWICImagingFactory.CreateComponentEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICImagingFactory::CreateComponentEnumerator


## -description


Creates an <a href="_com_IEnumUnknown">IEnumUnknown</a> object of the specified component types.


## -parameters




### -param componentTypes [in]

Type: <b>DWORD</b>

The types of <a href="https://msdn.microsoft.com/eff6b77c-ea4b-4476-8d75-dec5bb2e1745">WICComponentType</a> to enumerate.


### -param options [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/52cc0860-6164-4400-8e81-03eb0c44904e">WICComponentEnumerateOptions</a> used to enumerate the given component types. 


### -param ppIEnumUnknown [out]

Type: <b><a href="_com_IEnumUnknown">IEnumUnknown</a>**</b>

A pointer that receives a pointer to a new component enumerator.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Component types must be enumerated seperately. Combinations of component types and <b>WICAllComponents</b> are unsupported.



