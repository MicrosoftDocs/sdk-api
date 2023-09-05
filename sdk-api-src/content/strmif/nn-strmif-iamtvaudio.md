---
UID: NN:strmif.IAMTVAudio
title: IAMTVAudio (strmif.h)
description: The IAMTVAudio interface controls audio from a television source. The TV Audio filter implements this interface. Applications can use it to control television audio settings, including secondary audio program (SAP) and stereo or mono selection.
helpviewer_keywords: ["IAMTVAudio","IAMTVAudio interface [DirectShow]","IAMTVAudio interface [DirectShow]","described","IAMTVAudioInterface","dshow.iamtvaudio","strmif/IAMTVAudio"]
old-location: dshow\iamtvaudio.htm
tech.root: dshow
ms.assetid: de340594-4410-4896-b206-0f47d4035bc1
ms.date: 4/26/2023
ms.keywords: IAMTVAudio, IAMTVAudio interface [DirectShow], IAMTVAudio interface [DirectShow],described, IAMTVAudioInterface, dshow.iamtvaudio, strmif/IAMTVAudio
req.header: strmif.h
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
 - IAMTVAudio
 - strmif/IAMTVAudio
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
 - IAMTVAudio
---

# IAMTVAudio interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMTVAudio</code> interface controls audio from a television source. The <a href="/windows/desktop/DirectShow/tv-audio-filter">TV Audio</a> filter implements this interface. Applications can use it to control television audio settings, including secondary audio program (SAP) and stereo or mono selection.

## -inheritance

The <b>IAMTVAudio</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMTVAudio</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/analog-television">Analog Television</a>
