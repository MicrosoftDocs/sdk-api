---
UID: NF:wincodec.IWICImagingFactory.CreateStream
title: IWICImagingFactory::CreateStream
author: windows-sdk-content
description: Creates a new instance of the IWICStream class.
old-location: wic\_wic_codec_iwicimagingfactory_createstream.htm
tech.root: wic
ms.assetid: 1c2ecaf0-5222-4f9b-96fb-5d2da72d11d4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateStream, CreateStream method [Windows Imaging Component], CreateStream method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateStream method, IWICImagingFactory.CreateStream, IWICImagingFactory::CreateStream, _wic_codec_iwicimagingfactory_createstream, wic._wic_codec_iwicimagingfactory_createstream, wincodec/IWICImagingFactory::CreateStream
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
 - IWICImagingFactory.CreateStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICImagingFactory::CreateStream


## -description


Creates a new instance of the <a href="https://msdn.microsoft.com/bc398732-037d-4f48-940f-c70975447972">IWICStream</a> class.


## -parameters




### -param ppIWICStream [out]

Type: <b><a href="https://msdn.microsoft.com/bc398732-037d-4f48-940f-c70975447972">IWICStream</a>**</b>

A pointer that receives a pointer to a new <a href="https://msdn.microsoft.com/bc398732-037d-4f48-940f-c70975447972">IWICStream</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



