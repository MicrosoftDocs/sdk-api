---
UID: NF:vidcap.IVideoProcAmp.put_Hue
title: IVideoProcAmp::put_Hue (vidcap.h)
description: The put_Hue method sets the camera's hue setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","put_Hue method","IVideoProcAmp.put_Hue","IVideoProcAmp::put_Hue","IVideoProcAmpput_Hue","dshow.ivideoprocamp_put_hue","put_Hue","put_Hue method [DirectShow]","put_Hue method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::put_Hue"]
old-location: dshow\ivideoprocamp_put_hue.htm
tech.root: dshow
ms.assetid: 7b0926c3-4167-423d-ac5c-ac4df06948aa
ms.date: 4/26/2023
ms.keywords: IVideoProcAmp interface [DirectShow],put_Hue method, IVideoProcAmp.put_Hue, IVideoProcAmp::put_Hue, IVideoProcAmpput_Hue, dshow.ivideoprocamp_put_hue, put_Hue, put_Hue method [DirectShow], put_Hue method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Hue
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
 - IVideoProcAmp::put_Hue
 - vidcap/IVideoProcAmp::put_Hue
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
 - IVideoProcAmp.put_Hue
---

# IVideoProcAmp::put_Hue


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Hue</code> method sets the camera's hue setting.

## -parameters

### -param Value [in]

Specifies the hue setting, in units of degrees * 100. Theoretical values range from –180 degrees to +180 degrees, but the actual range depends on the camera. See <a href="/windows/desktop/api/vidcap/nf-vidcap-ivideoprocamp-getrange_hue">IVideoProcAmp::getRange_Hue</a>.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>