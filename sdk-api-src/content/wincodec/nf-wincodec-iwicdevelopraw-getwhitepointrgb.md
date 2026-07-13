---
UID: NF:wincodec.IWICDevelopRaw.GetWhitePointRGB
title: IWICDevelopRaw::GetWhitePointRGB (wincodec.h)
description: Gets the white point RGB values.
helpviewer_keywords: ["GetWhitePointRGB","GetWhitePointRGB method [Windows Imaging Component]","GetWhitePointRGB method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetWhitePointRGB method","IWICDevelopRaw.GetWhitePointRGB","IWICDevelopRaw::GetWhitePointRGB","_wic_codec_iwicdevelopraw_getwhitepointrgb","wic._wic_codec_iwicdevelopraw_getwhitepointrgb","wincodec/IWICDevelopRaw::GetWhitePointRGB"]
old-location: wic\_wic_codec_iwicdevelopraw_getwhitepointrgb.htm
tech.root: wic
ms.assetid: e163ba80-6ed2-4f03-b74f-07c96b478ac0
ms.date: 12/05/2018
ms.keywords: GetWhitePointRGB, GetWhitePointRGB method [Windows Imaging Component], GetWhitePointRGB method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetWhitePointRGB method, IWICDevelopRaw.GetWhitePointRGB, IWICDevelopRaw::GetWhitePointRGB, _wic_codec_iwicdevelopraw_getwhitepointrgb, wic._wic_codec_iwicdevelopraw_getwhitepointrgb, wincodec/IWICDevelopRaw::GetWhitePointRGB
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
 - IWICDevelopRaw::GetWhitePointRGB
 - wincodec/IWICDevelopRaw::GetWhitePointRGB
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
 - IWICDevelopRaw.GetWhitePointRGB
---

# IWICDevelopRaw::GetWhitePointRGB


## -description

Gets the white point RGB values.

## -parameters

### -param pRed [out]

Type: <b>UINT*</b>

A pointer that receives the red white point value.

### -param pGreen [out]

Type: <b>UINT*</b>

A pointer that receives the green white point value.

### -param pBlue [out]

Type: <b>UINT*</b>

A pointer that receives the blue white point value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

