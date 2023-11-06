---
UID: NF:vidcap.IVideoProcAmp.getRange_WhiteBalance
title: IVideoProcAmp::getRange_WhiteBalance (vidcap.h)
description: The getRange_WhiteBalance method returns the range of white balance settings supported by the camera, expressed as color temperature.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","getRange_WhiteBalance method","IVideoProcAmp.getRange_WhiteBalance","IVideoProcAmp::getRange_WhiteBalance","IVideoProcAmpgetRange_WhiteBalance","dshow.ivideoprocamp_getrange_whitebalance","getRange_WhiteBalance","getRange_WhiteBalance method [DirectShow]","getRange_WhiteBalance method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::getRange_WhiteBalance"]
old-location: dshow\ivideoprocamp_getrange_whitebalance.htm
tech.root: dshow
ms.assetid: 3c7a21ec-2aa5-4e00-8d7b-a13a366a3f17
ms.date: 4/26/2023
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_WhiteBalance method, IVideoProcAmp.getRange_WhiteBalance, IVideoProcAmp::getRange_WhiteBalance, IVideoProcAmpgetRange_WhiteBalance, dshow.ivideoprocamp_getrange_whitebalance, getRange_WhiteBalance, getRange_WhiteBalance method [DirectShow], getRange_WhiteBalance method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_WhiteBalance
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
 - IVideoProcAmp::getRange_WhiteBalance
 - vidcap/IVideoProcAmp::getRange_WhiteBalance
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
 - IVideoProcAmp.getRange_WhiteBalance
---

# IVideoProcAmp::getRange_WhiteBalance


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>getRange_WhiteBalance</code> method returns the range of white balance settings supported by the camera, expressed as color temperature.

## -parameters

### -param pMin [out]

Receives the minimum white balance, in degrees Kelvin.

### -param pMax [out]

Receives the maximum white balance, in degrees Kelvin.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default white balance.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>