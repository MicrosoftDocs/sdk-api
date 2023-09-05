---
UID: NF:mixerocx.IMixerOCX.OnDisplayChange
title: IMixerOCX::OnDisplayChange (mixerocx.h)
description: The OnDisplayChange method informs the Overlay Mixer that the monitor's display settings have changed. (Not implemented.).
helpviewer_keywords: ["IMixerOCX interface [DirectShow]","OnDisplayChange method","IMixerOCX.OnDisplayChange","IMixerOCX::OnDisplayChange","IMixerOCXOnDisplayChange","OnDisplayChange","OnDisplayChange method [DirectShow]","OnDisplayChange method [DirectShow]","IMixerOCX interface","dshow.imixerocx_ondisplaychange","mixerocx/IMixerOCX::OnDisplayChange"]
old-location: dshow\imixerocx_ondisplaychange.htm
tech.root: dshow
ms.assetid: 5d082ab6-6195-417b-ad0d-b8e97561b268
ms.date: 4/26/2023
ms.keywords: IMixerOCX interface [DirectShow],OnDisplayChange method, IMixerOCX.OnDisplayChange, IMixerOCX::OnDisplayChange, IMixerOCXOnDisplayChange, OnDisplayChange, OnDisplayChange method [DirectShow], OnDisplayChange method [DirectShow],IMixerOCX interface, dshow.imixerocx_ondisplaychange, mixerocx/IMixerOCX::OnDisplayChange
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
 - IMixerOCX::OnDisplayChange
 - mixerocx/IMixerOCX::OnDisplayChange
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
 - IMixerOCX.OnDisplayChange
---

# IMixerOCX::OnDisplayChange


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>OnDisplayChange</code> method informs the Overlay Mixer that the monitor's display settings have changed. (Not implemented.)

## -parameters

### -param ulBitsPerPixel [in]

Specifies the new bits per pixel setting.

### -param ulScreenWidth [in]

Specifies the new screen width in pixels.

### -param ulScreenHeight [in]

Specifies the new screen height in pixels.

## -returns

Returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>