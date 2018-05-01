---
UID: NF:wincodec.IWICBitmapDecoder.GetColorContexts
title: IWICBitmapDecoder::GetColorContexts method
author: windows-driver-content
description: Retrieves the IWICColorContext objects of the image.
old-location: wic\_wic_codec_iwicbitmapdecoder_getcolorcontexts.htm
old-project: wic
ms.assetid: 55fdf9c0-5fa4-46e2-b4d2-42b8d4c90887
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GetColorContexts method [Windows Imaging Component], GetColorContexts method [Windows Imaging Component], IWICBitmapDecoder interface, GetColorContexts,IWICBitmapDecoder.GetColorContexts, IWICBitmapDecoder, IWICBitmapDecoder interface [Windows Imaging Component], GetColorContexts method, IWICBitmapDecoder::GetColorContexts, _wic_codec_iwicbitmapdecoder_getcolorcontexts, wic._wic_codec_iwicbitmapdecoder_getcolorcontexts, wincodec/IWICBitmapDecoder::GetColorContexts
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.lib
-	Windowscodecs.dll
api_name:
-	IWICBitmapDecoder.GetColorContexts
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapDecoder::GetColorContexts method


## -description


Retrieves the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a> objects of the image.


## -parameters




### -param cCount [in]

Type: <b>UINT</b>

The number of color contexts to retrieve.

This value must be the size of, or smaller than, the size available to <i>ppIColorContexts</i>.


### -param ppIColorContexts [in, out]

Type: <b><a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>**</b>

A pointer that receives a pointer to the <a href="https://msdn.microsoft.com/b6817676-affb-4bb3-adba-e24e0b75ad10">IWICColorContext</a>.


### -param pcActualCount [out]

Type: <b>UINT*</b>

A pointer that receives the number of color contexts contained in the image.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



