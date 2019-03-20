---
UID: NF:wincodec.IWICBitmapDecoder.CopyPalette
title: IWICBitmapDecoder::CopyPalette (wincodec.h)
author: windows-sdk-content
description: Copies the decoder's IWICPalette .
old-location: wic\_wic_codec_iwicbitmapdecoder_copypalette.htm
tech.root: wic
ms.assetid: 4a387936-b045-42c7-b57c-1ac470640a14
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CopyPalette, CopyPalette method [Windows Imaging Component], CopyPalette method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],CopyPalette method, IWICBitmapDecoder.CopyPalette, IWICBitmapDecoder::CopyPalette, _wic_codec_iwicbitmapdecoder_copypalette, wic._wic_codec_iwicbitmapdecoder_copypalette, wincodec/IWICBitmapDecoder::CopyPalette
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
 - IWICBitmapDecoder.CopyPalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICBitmapDecoder::CopyPalette


## -description


Copies the decoder's <a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a> .


## -parameters




### -param pIPalette [in]

Type: <b><a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a>*</b>

An<a href="https://msdn.microsoft.com/cb0e4f92-4aff-48c7-af62-5f7154539289">IWICPalette</a> to which the decoder's global palette is to be copied. Use <a href="https://msdn.microsoft.com/135440ee-ea70-40da-9ee1-618a8e10170a">CreatePalette</a> to create the destination palette before calling <b>CopyPalette</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>CopyPalette</b> returns a global palette (a palette that applies to all the frames in the image) if there is one; otherwise, it returns WINCODEC_ERR_PALETTEUNAVAILABLE. If an image doesn't have a global palette, it may still have a frame-level palette, which can be retrieved using <a href="https://msdn.microsoft.com/5e45ca4a-2d14-4829-9542-9cfc3e4b0d73">IWICBitmapFrameDecode::CopyPalette</a>.



