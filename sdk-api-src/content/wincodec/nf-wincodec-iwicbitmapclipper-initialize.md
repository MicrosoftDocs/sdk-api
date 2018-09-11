---
UID: NF:wincodec.IWICBitmapClipper.Initialize
title: IWICBitmapClipper::Initialize
author: windows-sdk-content
description: Initializes the bitmap clipper with the provided parameters.
old-location: wic\_wic_codec_iwicbitmapclipper_initialize.htm
tech.root: wic
ms.assetid: a0b8a572-d947-4d57-9214-d39085a78b6e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWICBitmapClipper interface [Windows Imaging Component],Initialize method, IWICBitmapClipper.Initialize, IWICBitmapClipper::Initialize, Initialize, Initialize method [Windows Imaging Component], Initialize method [Windows Imaging Component],IWICBitmapClipper interface, _wic_codec_iwicbitmapclipper_initialize, wic._wic_codec_iwicbitmapclipper_initialize, wincodec/IWICBitmapClipper::Initialize
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
 - IWICBitmapClipper.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapClipper::Initialize


## -description


Initializes the bitmap clipper with the provided parameters.


## -parameters




### -param pISource [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

he input bitmap source.


### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/e07c26bf-b645-4382-bb93-8472ba397026">WICRect</a>*</b>

The rectangle of the bitmap source to clip.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



