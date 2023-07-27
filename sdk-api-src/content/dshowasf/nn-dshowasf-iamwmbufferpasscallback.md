---
UID: NN:dshowasf.IAMWMBufferPassCallback
title: IAMWMBufferPassCallback (dshowasf.h)
description: The IAMWMBufferPassCallback interface is provided for advanced scenarios in which applications need access to an INSSBuffer3 sample before it is passed downstream for further processing.
helpviewer_keywords: ["IAMWMBufferPassCallback","IAMWMBufferPassCallback interface [windows Media Format]","IAMWMBufferPassCallback interface [windows Media Format]","described","IAMWMBufferPassCallbackInterface","dshowasf/IAMWMBufferPassCallback","wmformat.iamwmbufferpasscallback"]
old-location: wmformat\iamwmbufferpasscallback.htm
tech.root: wmformat
ms.assetid: 5bf0ae2e-504b-471b-bfc9-aa48f534e03f
ms.date: 4/26/2023
ms.keywords: IAMWMBufferPassCallback, IAMWMBufferPassCallback interface [windows Media Format], IAMWMBufferPassCallback interface [windows Media Format],described, IAMWMBufferPassCallbackInterface, dshowasf/IAMWMBufferPassCallback, wmformat.iamwmbufferpasscallback
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Requires Dshowasf.h, Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: 
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
 - IAMWMBufferPassCallback
 - dshowasf/IAMWMBufferPassCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dshowasf.h
api_name:
 - IAMWMBufferPassCallback
---

# IAMWMBufferPassCallback interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IAMWMBufferPassCallback</b> interface is provided for advanced scenarios in which applications need access to an <b>INSSBuffer3</b> sample before it is passed downstream for further processing. Use this technique to set or retrieve data unit extensions such as the SMPTE time code for each sample. One common use for this interface is to force key-frame insertion in a variable bit rate video stream during file writing. To do this, you must set the <a href="/windows/desktop/wmformat/wmformat-glossary">cleanpoint</a> property on individual <b>INSSBuffer3</b> samples. This interface is implemented by applications and called by the WM ASF Writer or <a href="/windows/desktop/wmformat/wm-asf-reader-filter">WM ASF Reader</a> filter each time a new sample is delivered to the filter.

## -inheritance

The <b>IAMWMBufferPassCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMWMBufferPassCallback</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/directshow-qasf-reference">DirectShow QASF Reference</a>



<a href="/previous-versions/windows/desktop/legacy/dd798276(v=vs.85)">IAMWMBufferPass Interface</a>



<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3 Interface</a>
