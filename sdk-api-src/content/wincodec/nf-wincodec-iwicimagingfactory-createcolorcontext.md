---
UID: NF:wincodec.IWICImagingFactory.CreateColorContext
title: IWICImagingFactory::CreateColorContext
author: windows-sdk-content
description: Creates a new instance of the IWICColorContext class.
old-location: wic\_wic_codec_iwicimagingfactory_createcolorcontext.htm
tech.root: wic
ms.assetid: 60ae0ec4-2bf4-43f0-9882-ff8b6f5f5923
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateColorContext, CreateColorContext method [Windows Imaging Component], CreateColorContext method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateColorContext method, IWICImagingFactory.CreateColorContext, IWICImagingFactory::CreateColorContext, _wic_codec_iwicimagingfactory_createcolorcontext, wic._wic_codec_iwicimagingfactory_createcolorcontext, wincodec/IWICImagingFactory::CreateColorContext
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
 - IWICImagingFactory.CreateColorContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICImagingFactory::CreateColorContext


## -description


Creates a new instance of the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> class.


## -parameters




### -param ppIWICColorContext [out]

Type: <b><a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



