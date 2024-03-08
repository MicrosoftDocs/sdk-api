---
UID: NF:mixerocx.IMixerOCX.UnAdvise
title: IMixerOCX::UnAdvise (mixerocx.h)
description: The UnAdvise method instructs the Overlay Mixer to release its pointer to the client's IMixerOCXNotify interface.
helpviewer_keywords: ["IMixerOCX interface [DirectShow]","UnAdvise method","IMixerOCX.UnAdvise","IMixerOCX::UnAdvise","IMixerOCXUnAdvise","UnAdvise","UnAdvise method [DirectShow]","UnAdvise method [DirectShow]","IMixerOCX interface","dshow.imixerocx_unadvise","mixerocx/IMixerOCX::UnAdvise"]
old-location: dshow\imixerocx_unadvise.htm
tech.root: dshow
ms.assetid: 9c2837c6-ee0f-45f4-b98a-9b8957e75b48
ms.date: 4/26/2023
ms.keywords: IMixerOCX interface [DirectShow],UnAdvise method, IMixerOCX.UnAdvise, IMixerOCX::UnAdvise, IMixerOCXUnAdvise, UnAdvise, UnAdvise method [DirectShow], UnAdvise method [DirectShow],IMixerOCX interface, dshow.imixerocx_unadvise, mixerocx/IMixerOCX::UnAdvise
req.header: mixerocx.h
req.include-header: 
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
 - IMixerOCX::UnAdvise
 - mixerocx/IMixerOCX::UnAdvise
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
 - IMixerOCX.UnAdvise
---

# IMixerOCX::UnAdvise


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>UnAdvise</code> method instructs the Overlay Mixer to release its pointer to the client's <a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify">IMixerOCXNotify</a> interface.



## -returns

If the method succeeds, it returns S_OK.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>
