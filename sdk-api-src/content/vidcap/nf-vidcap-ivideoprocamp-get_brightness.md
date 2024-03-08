---
UID: NF:vidcap.IVideoProcAmp.get_Brightness
title: IVideoProcAmp::get_Brightness (vidcap.h)
description: The get_Brightness method returns the camera's brightness setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","get_Brightness method","IVideoProcAmp.get_Brightness","IVideoProcAmp::get_Brightness","IVideoProcAmpget_Brightness","dshow.ivideoprocamp_get_brightness","get_Brightness","get_Brightness method [DirectShow]","get_Brightness method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::get_Brightness"]
old-location: dshow\ivideoprocamp_get_brightness.htm
tech.root: dshow
ms.assetid: b0e3b7cf-c133-4b47-8209-1014d1e3d671
ms.date: 4/26/2023
ms.keywords: IVideoProcAmp interface [DirectShow],get_Brightness method, IVideoProcAmp.get_Brightness, IVideoProcAmp::get_Brightness, IVideoProcAmpget_Brightness, dshow.ivideoprocamp_get_brightness, get_Brightness, get_Brightness method [DirectShow], get_Brightness method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::get_Brightness
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
 - IVideoProcAmp::get_Brightness
 - vidcap/IVideoProcAmp::get_Brightness
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
 - IVideoProcAmp.get_Brightness
---

# IVideoProcAmp::get_Brightness


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_Brightness</code> method returns the camera's brightness setting.

## -parameters

### -param pValue [out]

Receives the brightness setting. Larger values indicate increased brightness.

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>