---
UID: NF:vidcap.IVideoProcAmp.getRange_ColorEnable
title: IVideoProcAmp::getRange_ColorEnable (vidcap.h)
description: The getRange_ColorEnable method returns the range of color-enable settings supported by the camera.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","getRange_ColorEnable method","IVideoProcAmp.getRange_ColorEnable","IVideoProcAmp::getRange_ColorEnable","IVideoProcAmpgetRange_ColorEnable","dshow.ivideoprocamp_getrange_colorenable","getRange_ColorEnable","getRange_ColorEnable method [DirectShow]","getRange_ColorEnable method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::getRange_ColorEnable"]
old-location: dshow\ivideoprocamp_getrange_colorenable.htm
tech.root: dshow
ms.assetid: d9041f2a-cf38-419b-be8f-a55599b9a1d9
ms.date: 4/26/2023
ms.keywords: IVideoProcAmp interface [DirectShow],getRange_ColorEnable method, IVideoProcAmp.getRange_ColorEnable, IVideoProcAmp::getRange_ColorEnable, IVideoProcAmpgetRange_ColorEnable, dshow.ivideoprocamp_getrange_colorenable, getRange_ColorEnable, getRange_ColorEnable method [DirectShow], getRange_ColorEnable method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::getRange_ColorEnable
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
 - IVideoProcAmp::getRange_ColorEnable
 - vidcap/IVideoProcAmp::getRange_ColorEnable
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
 - IVideoProcAmp.getRange_ColorEnable
---

# IVideoProcAmp::getRange_ColorEnable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>getRange_ColorEnable</code> method returns the range of color-enable settings supported by the camera.

## -parameters

### -param pMin [out]

Receives the minimum color-enable setting.

### -param pMax [out]

Receives the maximum color-enable setting.

### -param pSteppingDelta [out]

Receives the smallest step between settings.

### -param pDefault [out]

Receives the default color-enable setting.

### -param pCapsFlag [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>