---
UID: NN:wincodec.IWICProgressiveLevelControl
title: IWICProgressiveLevelControl (wincodec.h)
description: Exposes methods for obtaining information about and controlling progressive decoding.
helpviewer_keywords: ["IWICProgressiveLevelControl","IWICProgressiveLevelControl interface [Windows Imaging Component]","IWICProgressiveLevelControl interface [Windows Imaging Component]","described","_wic_codec_iwicprogressivelevelcontrol","wic._wic_codec_iwicprogressivelevelcontrol","wincodec/IWICProgressiveLevelControl"]
old-location: wic\_wic_codec_iwicprogressivelevelcontrol.htm
tech.root: wic
ms.assetid: d77244bc-b9d4-4b7d-b718-4ee38de46614
ms.date: 12/05/2018
ms.keywords: IWICProgressiveLevelControl, IWICProgressiveLevelControl interface [Windows Imaging Component], IWICProgressiveLevelControl interface [Windows Imaging Component],described, _wic_codec_iwicprogressivelevelcontrol, wic._wic_codec_iwicprogressivelevelcontrol, wincodec/IWICProgressiveLevelControl
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
 - IWICProgressiveLevelControl
 - wincodec/IWICProgressiveLevelControl
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
 - IWICProgressiveLevelControl
---

# IWICProgressiveLevelControl interface


## -description

Exposes methods for obtaining information about and controlling progressive decoding.

## -inheritance

The <b>IWICProgressiveLevelControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICProgressiveLevelControl</b> also has these types of members:

## -remarks

Images can only be progressively decoded if they were progressively encoded. Progressive images automatically start at the highest (best quality) progressive level. The caller must manually set the decoder to a lower progressive level.

E_NOTIMPL is returned if the codec does not support progressive level decoding.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-progressive-decoding">Progressive Decoding Overview</a>



<a href="/windows/desktop/wic/-wic-sample-progressive-decoding">WIC Progressive Decoding Sample</a>
