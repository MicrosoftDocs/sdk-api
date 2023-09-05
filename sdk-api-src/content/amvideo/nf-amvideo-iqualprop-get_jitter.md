---
UID: NF:amvideo.IQualProp.get_Jitter
title: IQualProp::get_Jitter (amvideo.h)
description: The get_Jitter method gets the jitter (variation in time) between successive frames delivered to the video renderer.
helpviewer_keywords: ["IQualProp interface [DirectShow]","get_Jitter method","IQualProp.get_Jitter","IQualProp::get_Jitter","IQualPropget_Jitter","amvideo/IQualProp::get_Jitter","dshow.iqualprop_get_jitter","get_Jitter","get_Jitter method [DirectShow]","get_Jitter method [DirectShow]","IQualProp interface"]
old-location: dshow\iqualprop_get_jitter.htm
tech.root: dshow
ms.assetid: e1f6e93f-58d6-41b4-b16f-e9f02bfec0fe
ms.date: 4/26/2023
ms.keywords: IQualProp interface [DirectShow],get_Jitter method, IQualProp.get_Jitter, IQualProp::get_Jitter, IQualPropget_Jitter, amvideo/IQualProp::get_Jitter, dshow.iqualprop_get_jitter, get_Jitter, get_Jitter method [DirectShow], get_Jitter method [DirectShow],IQualProp interface
req.header: amvideo.h
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
 - IQualProp::get_Jitter
 - amvideo/IQualProp::get_Jitter
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
 - IQualProp.get_Jitter
---

# IQualProp::get_Jitter


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>get_Jitter</b> method gets the jitter (variation in time) between successive frames delivered to the video renderer.

## -parameters

### -param iJitter

Receives the standard deviation of the interframe time, in milliseconds.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-iqualprop">IQualProp Interface</a>