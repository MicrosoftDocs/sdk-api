---
UID: NF:amvideo.IQualProp.get_AvgFrameRate
title: IQualProp::get_AvgFrameRate (amvideo.h)
description: The get_AvgFrameRate method retrieves the actual average frame rate since streaming started.
helpviewer_keywords: ["IQualProp interface [DirectShow]","get_AvgFrameRate method","IQualProp.get_AvgFrameRate","IQualProp::get_AvgFrameRate","IQualPropget_AvgFrameRate","amvideo/IQualProp::get_AvgFrameRate","dshow.iqualprop_get_avgframerate","get_AvgFrameRate","get_AvgFrameRate method [DirectShow]","get_AvgFrameRate method [DirectShow]","IQualProp interface"]
old-location: dshow\iqualprop_get_avgframerate.htm
tech.root: dshow
ms.assetid: 31e326e2-56de-4c7c-b26a-836c9fc76342
ms.date: 4/26/2023
ms.keywords: IQualProp interface [DirectShow],get_AvgFrameRate method, IQualProp.get_AvgFrameRate, IQualProp::get_AvgFrameRate, IQualPropget_AvgFrameRate, amvideo/IQualProp::get_AvgFrameRate, dshow.iqualprop_get_avgframerate, get_AvgFrameRate, get_AvgFrameRate method [DirectShow], get_AvgFrameRate method [DirectShow],IQualProp interface
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
 - IQualProp::get_AvgFrameRate
 - amvideo/IQualProp::get_AvgFrameRate
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
 - IQualProp.get_AvgFrameRate
---

# IQualProp::get_AvgFrameRate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_AvgFrameRate</code> method retrieves the actual average frame rate since streaming started.

## -parameters

### -param piAvgFrameRate

Pointer to a variable that receives the actual number of frames per second, multiplied by 100. For example, an average frame rate of 30 frames per second will be represented as 3000.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The actual frame rate during playback might be less than the authored frame rate. For more information on actual versus authored frame rates, see the Remarks section for the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-iqualprop">IQualProp Interface</a>