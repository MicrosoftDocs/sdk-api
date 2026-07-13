---
UID: NF:dshowasf.IAMWMBufferPassCallback.Notify
title: IAMWMBufferPassCallback::Notify (dshowasf.h)
description: The Notify method is called by the pin for each buffer that is delivered during streaming.
helpviewer_keywords: ["IAMWMBufferPassCallback interface [windows Media Format]","Notify method","IAMWMBufferPassCallback.Notify","IAMWMBufferPassCallback::Notify","IAMWMBufferPassCallbackNotify","Notify","Notify method [windows Media Format]","Notify method [windows Media Format]","IAMWMBufferPassCallback interface","dshowasf/IAMWMBufferPassCallback::Notify","wmformat.iamwmbufferpasscallback_notify"]
old-location: wmformat\iamwmbufferpasscallback_notify.htm
tech.root: wmformat
ms.assetid: 3f252754-c784-4ffd-bcfc-fab73fa02b9a
ms.date: 4/26/2023
ms.keywords: IAMWMBufferPassCallback interface [windows Media Format],Notify method, IAMWMBufferPassCallback.Notify, IAMWMBufferPassCallback::Notify, IAMWMBufferPassCallbackNotify, Notify, Notify method [windows Media Format], Notify method [windows Media Format],IAMWMBufferPassCallback interface, dshowasf/IAMWMBufferPassCallback::Notify, wmformat.iamwmbufferpasscallback_notify
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
 - IAMWMBufferPassCallback::Notify
 - dshowasf/IAMWMBufferPassCallback::Notify
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
 - IAMWMBufferPassCallback.Notify
---

# IAMWMBufferPassCallback::Notify


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Notify</b> method is called by the pin for each buffer that is delivered during streaming.

## -parameters

### -param pNSSBuffer3 [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3</a> interface exposed on the media sample.

### -param pPin [in]

Pointer to the pin associated with the media stream that the sample belongs to.

### -param prtStart [in]

Start time of the sample.

### -param prtEnd [in]

End time of the sample.

## -returns

No particular return value is specified. The calling pin ignores the <b>HRESULT</b>.

## -remarks

This method enables an application to examine and act on information in the media buffer before the buffer contents are processed. The application is responsible for knowing the media type on the pin. This information can be obtained by first getting the stream information from the profile and then calling <a href="/windows/desktop/wmformat/iconfigasfwriter2-streamnumfrompin">IConfigAsfWriter2::StreamNumFromPin</a> method to determine which pin is associated with each stream.

## -see-also

<a href="/windows/desktop/wmformat/directshow-qasf-reference">DirectShow QASF Reference</a>



<a href="/previous-versions/windows/desktop/legacy/dd798277(v=vs.85)">IAMWMBufferPassCallback Interface</a>



<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3 Interface</a>