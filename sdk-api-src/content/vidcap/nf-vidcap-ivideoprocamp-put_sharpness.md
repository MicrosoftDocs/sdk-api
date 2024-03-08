---
UID: NF:vidcap.IVideoProcAmp.put_Sharpness
title: IVideoProcAmp::put_Sharpness (vidcap.h)
description: The put_Sharpness method sets the camera's sharpness setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","put_Sharpness method","IVideoProcAmp.put_Sharpness","IVideoProcAmp::put_Sharpness","IVideoProcAmpput_Sharpness","dshow.ivideoprocamp_put_sharpness","put_Sharpness","put_Sharpness method [DirectShow]","put_Sharpness method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::put_Sharpness"]
old-location: dshow\ivideoprocamp_put_sharpness.htm
tech.root: dshow
ms.assetid: a47e8f21-29ec-4845-97b2-1a9d6478afa6
ms.date: 4/26/2023
ms.keywords: IVideoProcAmp interface [DirectShow],put_Sharpness method, IVideoProcAmp.put_Sharpness, IVideoProcAmp::put_Sharpness, IVideoProcAmpput_Sharpness, dshow.ivideoprocamp_put_sharpness, put_Sharpness, put_Sharpness method [DirectShow], put_Sharpness method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Sharpness
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
 - IVideoProcAmp::put_Sharpness
 - vidcap/IVideoProcAmp::put_Sharpness
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
 - IVideoProcAmp.put_Sharpness
---

# IVideoProcAmp::put_Sharpness


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Sharpness</code> method sets the camera's sharpness setting.

## -parameters

### -param Value [in]

Specifies the sharpness setting. Larger values indicate increasing sharpness.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>