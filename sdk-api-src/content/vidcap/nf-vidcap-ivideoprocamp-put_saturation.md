---
UID: NF:vidcap.IVideoProcAmp.put_Saturation
title: IVideoProcAmp::put_Saturation (vidcap.h)
description: The put_Saturation method sets the camera's saturation setting.
helpviewer_keywords: ["IVideoProcAmp interface [DirectShow]","put_Saturation method","IVideoProcAmp.put_Saturation","IVideoProcAmp::put_Saturation","IVideoProcAmpput_Saturation","dshow.ivideoprocamp_put_saturation","put_Saturation","put_Saturation method [DirectShow]","put_Saturation method [DirectShow]","IVideoProcAmp interface","vidcap/IVideoProcAmp::put_Saturation"]
old-location: dshow\ivideoprocamp_put_saturation.htm
tech.root: dshow
ms.assetid: 7167fcac-b0c8-444e-a6a9-7ff9a603cc58
ms.date: 4/26/2023
ms.keywords: IVideoProcAmp interface [DirectShow],put_Saturation method, IVideoProcAmp.put_Saturation, IVideoProcAmp::put_Saturation, IVideoProcAmpput_Saturation, dshow.ivideoprocamp_put_saturation, put_Saturation, put_Saturation method [DirectShow], put_Saturation method [DirectShow],IVideoProcAmp interface, vidcap/IVideoProcAmp::put_Saturation
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
 - IVideoProcAmp::put_Saturation
 - vidcap/IVideoProcAmp::put_Saturation
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
 - IVideoProcAmp.put_Saturation
---

# IVideoProcAmp::put_Saturation


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_Saturation</code> method sets the camera's saturation setting.

## -parameters

### -param Value [in]

Specifies the saturation setting. Larger values indicate greater saturation. The value zero indicates grayscale.

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-videoprocampflags">VideoProcAmpFlags</a>. If the VideoProcAmp_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-ivideoprocamp">IVideoProcAmp Interface</a>