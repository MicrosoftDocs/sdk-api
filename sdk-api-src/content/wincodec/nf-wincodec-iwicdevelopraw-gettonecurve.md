---
UID: NF:wincodec.IWICDevelopRaw.GetToneCurve
title: IWICDevelopRaw::GetToneCurve (wincodec.h)
description: Gets the tone curve of the raw image.
helpviewer_keywords: ["GetToneCurve","GetToneCurve method [Windows Imaging Component]","GetToneCurve method [Windows Imaging Component]","IWICDevelopRaw interface","IWICDevelopRaw interface [Windows Imaging Component]","GetToneCurve method","IWICDevelopRaw.GetToneCurve","IWICDevelopRaw::GetToneCurve","_wic_codec_iwicdevelopraw_gettonecurve","wic._wic_codec_iwicdevelopraw_gettonecurve","wincodec/IWICDevelopRaw::GetToneCurve"]
old-location: wic\_wic_codec_iwicdevelopraw_gettonecurve.htm
tech.root: wic
ms.assetid: 651f9efb-145a-400b-8d7c-255aee67c385
ms.date: 12/05/2018
ms.keywords: GetToneCurve, GetToneCurve method [Windows Imaging Component], GetToneCurve method [Windows Imaging Component],IWICDevelopRaw interface, IWICDevelopRaw interface [Windows Imaging Component],GetToneCurve method, IWICDevelopRaw.GetToneCurve, IWICDevelopRaw::GetToneCurve, _wic_codec_iwicdevelopraw_gettonecurve, wic._wic_codec_iwicdevelopraw_gettonecurve, wincodec/IWICDevelopRaw::GetToneCurve
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
 - IWICDevelopRaw::GetToneCurve
 - wincodec/IWICDevelopRaw::GetToneCurve
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
 - IWICDevelopRaw.GetToneCurve
---

# IWICDevelopRaw::GetToneCurve


## -description

Gets the tone curve of the raw image.

## -parameters

### -param cbToneCurveBufferSize [in]

Type: <b>UINT</b>

The size of the <i>pToneCurve</i> buffer.

### -param pToneCurve [out]

Type: <b><a href="/windows/desktop/api/wincodec/ns-wincodec-wicrawtonecurve">WICRawToneCurve</a>*</b>

A pointer that receives the <a href="/windows/desktop/api/wincodec/ns-wincodec-wicrawtonecurve">WICRawToneCurve</a> of the raw image.

### -param pcbActualToneCurveBufferSize [out]

Type: <b>UINT*</b>

A pointer that receives the size needed to obtain the tone curve structure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.