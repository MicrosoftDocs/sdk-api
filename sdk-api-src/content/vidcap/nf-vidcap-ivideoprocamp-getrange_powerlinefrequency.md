---
UID: NF:vidcap.IVideoProcAmp.getRange_PowerlineFrequency
title: IVideoProcAmp::getRange_PowerlineFrequency (vidcap.h)
description: The getRange_PowerlineFrequency method returns the range of power line frequency settings supported by the camera.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","getRange_PowerlineFrequency method","IVideoProcAmp.getRange_PowerlineFrequency","IVideoProcAmp::getRange_PowerlineFrequency","IVideoProcAmpgetRange_PowerlineFrequency","dshow.ivideoprocamp_getrange_powerlinefrequency","getRange_PowerlineFrequency","getRange_PowerlineFrequency method [DirectShow]","getRange_PowerlineFrequency method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::getRange_PowerlineFrequency"]
old-location: dshow\ivideoprocamp_getrange_powerlinefrequency.htm
tech.root: dshow
ms.assetid: f6bb1df3-d033-4627-b5ea-574a2ebf43aa
ms.date: 4/26/2023
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_PowerlineFrequency method, IVideoProcAmp.getRange_PowerlineFrequency, IVideoProcAmp::getRange_PowerlineFrequency, IVideoProcAmpgetRange_PowerlineFrequency, dshow.ivideoprocamp_getrange_powerlinefrequency, getRange_PowerlineFrequency, getRange_PowerlineFrequency method [DirectShow], getRange_PowerlineFrequency method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_PowerlineFrequency
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVideoProcAmp::getRange_PowerlineFrequency
 - vidcap/IVideoProcAmp::getRange_PowerlineFrequency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vidcap.h
api_name:
 - IVideoProcAmp.getRange_PowerlineFrequency
---

# IVideoProcAmp::getRange_PowerlineFrequency


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>getRange_PowerlineFrequency</code> method returns the range of power line frequency settings supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum power line frequency setting.

### -param pMax [out]

Receives the maximum power line frequency setting.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default power line frequency setting.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>