---
UID: NF:strmif.IAMTuner.get_Mode
title: IAMTuner::get_Mode (strmif.h)
description: The get_Mode method retrieves the current mode on a multifunction tuner.
helpviewer_keywords: ["IAMTuner interface [DirectShow]","get_Mode method","IAMTuner.get_Mode","IAMTuner::get_Mode","IAMTunerget_Mode","dshow.iamtuner_get_mode","get_Mode","get_Mode method [DirectShow]","get_Mode method [DirectShow]","IAMTuner interface","strmif/IAMTuner::get_Mode"]
old-location: dshow\iamtuner_get_mode.htm
tech.root: dshow
ms.assetid: 9a5f4cd8-8fde-4777-b9b6-caa7860b005c
ms.date: 4/26/2023
ms.keywords: IAMTuner interface [DirectShow],get_Mode method, IAMTuner.get_Mode, IAMTuner::get_Mode, IAMTunerget_Mode, dshow.iamtuner_get_mode, get_Mode, get_Mode method [DirectShow], get_Mode method [DirectShow],IAMTuner interface, strmif/IAMTuner::get_Mode
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTuner::get_Mode
 - strmif/IAMTuner::get_Mode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTuner.get_Mode
---

# IAMTuner::get_Mode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Mode</code> method retrieves the current mode on a multifunction tuner.

## -parameters

### -param plMode [out]

Pointer to a variable that receives a flag indicating the current mode setting. The possible values are defined in the [AMTunerModeType](/windows/desktop/api/strmif/ne-strmif-amtunermodetype) enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>