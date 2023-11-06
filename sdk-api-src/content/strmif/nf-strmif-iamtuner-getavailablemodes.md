---
UID: NF:strmif.IAMTuner.GetAvailableModes
title: IAMTuner::GetAvailableModes (strmif.h)
description: The GetAvailableModes method retrieves the tuner's supported modes.
helpviewer_keywords: ["GetAvailableModes","GetAvailableModes method [DirectShow]","GetAvailableModes method [DirectShow]","IAMTuner interface","IAMTuner interface [DirectShow]","GetAvailableModes method","IAMTuner.GetAvailableModes","IAMTuner::GetAvailableModes","IAMTunerGetAvailableModes","dshow.iamtuner_getavailablemodes","strmif/IAMTuner::GetAvailableModes"]
old-location: dshow\iamtuner_getavailablemodes.htm
tech.root: dshow
ms.assetid: 74025309-2aab-4e0f-95bc-8e6a1e2a5bb4
ms.date: 4/26/2023
ms.keywords: GetAvailableModes, GetAvailableModes method [DirectShow], GetAvailableModes method [DirectShow],IAMTuner interface, IAMTuner interface [DirectShow],GetAvailableModes method, IAMTuner.GetAvailableModes, IAMTuner::GetAvailableModes, IAMTunerGetAvailableModes, dshow.iamtuner_getavailablemodes, strmif/IAMTuner::GetAvailableModes
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
 - IAMTuner::GetAvailableModes
 - strmif/IAMTuner::GetAvailableModes
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
 - IAMTuner.GetAvailableModes
---

# IAMTuner::GetAvailableModes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAvailableModes</code> method retrieves the tuner's supported modes.

## -parameters

### -param plModes [out]

Pointer to a variable that receives any combination of the values as specified in the [AMTunerModeType](/windows/desktop/api/strmif/ne-strmif-amtunermodetype) enumeration.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtuner">IAMTuner Interface</a>