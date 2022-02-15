---
UID: NF:wincodec.IWICDevelopRaw.SetToneCurve
title: IWICDevelopRaw::SetToneCurve (wincodec.h)
description: Sets the tone curve for the raw image.
helpviewer_keywords: ["IWICDevelopRaw interface [Windows Imaging Component]","SetToneCurve method","IWICDevelopRaw.SetToneCurve","IWICDevelopRaw::SetToneCurve","SetToneCurve","SetToneCurve method [Windows Imaging Component]","SetToneCurve method [Windows Imaging Component]","IWICDevelopRaw interface","_wic_codec_iwicdevelopraw_settonecurve","wic._wic_codec_iwicdevelopraw_settonecurve","wincodec/IWICDevelopRaw::SetToneCurve"]
old-location: wic\_wic_codec_iwicdevelopraw_settonecurve.htm
tech.root: wic
ms.assetid: cfb0b67d-7eb1-4bbb-90be-33ca82b9460f
ms.date: 12/05/2018
ms.keywords: IWICDevelopRaw interface [Windows Imaging Component],SetToneCurve method, IWICDevelopRaw.SetToneCurve, IWICDevelopRaw::SetToneCurve, SetToneCurve, SetToneCurve method [Windows Imaging Component], SetToneCurve method [Windows Imaging Component],IWICDevelopRaw interface, _wic_codec_iwicdevelopraw_settonecurve, wic._wic_codec_iwicdevelopraw_settonecurve, wincodec/IWICDevelopRaw::SetToneCurve
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
 - IWICDevelopRaw::SetToneCurve
 - wincodec/IWICDevelopRaw::SetToneCurve
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
 - IWICDevelopRaw.SetToneCurve
---

# IWICDevelopRaw::SetToneCurve


## -description

Sets the tone curve for the raw image.

## -parameters

### -param cbToneCurveSize [in]

Type: <b>UINT</b>

The size of the <i>pToneCurve</i> structure.

### -param pToneCurve [in]

Type: <b>const <a href="/windows/desktop/api/wincodec/ns-wincodec-wicrawtonecurve">WICRawToneCurve</a>*</b>

The desired tone curve.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.