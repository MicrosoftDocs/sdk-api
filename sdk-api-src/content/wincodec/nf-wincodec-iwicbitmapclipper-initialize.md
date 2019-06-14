---
UID: NF:wincodec.IWICBitmapClipper.Initialize
title: IWICBitmapClipper::Initialize (wincodec.h)
author: windows-sdk-content
description: Initializes the bitmap clipper with the provided parameters.
old-location: wic\_wic_codec_iwicbitmapclipper_initialize.htm
tech.root: wic
ms.assetid: a0b8a572-d947-4d57-9214-d39085a78b6e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICBitmapClipper interface [Windows Imaging Component],Initialize method, IWICBitmapClipper.Initialize, IWICBitmapClipper::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapClipper interface, _wic_codec_iwicbitmapclipper_initialize, wic._wic_codec_iwicbitmapclipper_initialize, wincodec/IWICBitmapClipper::Initialize
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
 - IWICBitmapClipper.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapClipper::Initialize


## -description


Initializes the bitmap clipper with the provided parameters.


## -parameters




### -param pISource [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

he input bitmap source.


### -param prc [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/ns-wincodec-wicrect">WICRect</a>*</b>

The rectangle of the bitmap source to clip.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



