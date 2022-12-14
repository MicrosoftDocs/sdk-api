---
UID: NF:wincodec.IWICProgressiveLevelControl.GetCurrentLevel
title: IWICProgressiveLevelControl::GetCurrentLevel (wincodec.h)
description: Gets the decoder's current progressive level.
helpviewer_keywords: ["GetCurrentLevel","GetCurrentLevel method [Windows Imaging Component]","GetCurrentLevel method [Windows Imaging Component]","IWICProgressiveLevelControl interface","IWICProgressiveLevelControl interface [Windows Imaging Component]","GetCurrentLevel method","IWICProgressiveLevelControl.GetCurrentLevel","IWICProgressiveLevelControl::GetCurrentLevel","_wic_codec_iwicprogressivelevelcontrol_getcurrentlevel","wic._wic_codec_iwicprogressivelevelcontrol_getcurrentlevel","wincodec/IWICProgressiveLevelControl::GetCurrentLevel"]
old-location: wic\_wic_codec_iwicprogressivelevelcontrol_getcurrentlevel.htm
tech.root: wic
ms.assetid: c6f848a0-e373-4344-8923-3ad77165ef71
ms.date: 12/05/2018
ms.keywords: GetCurrentLevel, GetCurrentLevel method [Windows Imaging Component], GetCurrentLevel method [Windows Imaging Component],IWICProgressiveLevelControl interface, IWICProgressiveLevelControl interface [Windows Imaging Component],GetCurrentLevel method, IWICProgressiveLevelControl.GetCurrentLevel, IWICProgressiveLevelControl::GetCurrentLevel, _wic_codec_iwicprogressivelevelcontrol_getcurrentlevel, wic._wic_codec_iwicprogressivelevelcontrol_getcurrentlevel, wincodec/IWICProgressiveLevelControl::GetCurrentLevel
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICProgressiveLevelControl::GetCurrentLevel
 - wincodec/IWICProgressiveLevelControl::GetCurrentLevel
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
 - IWICProgressiveLevelControl.GetCurrentLevel
---

# IWICProgressiveLevelControl::GetCurrentLevel


## -description

Gets the decoder's current progressive level.

## -parameters

### -param pnLevel [out, retval]

Type: <b>UINT*</b>

Indicates the current level specified.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The level always defaults to the highest progressive level. In order to decode a lower progressive level, <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel">SetCurrentLevel</a> must first be called.

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicprogressivelevelcontrol">IWICProgressiveLevelControl</a>



<a href="/windows/desktop/wic/-wic-progressive-decoding">Progressive Decoding Overview</a>