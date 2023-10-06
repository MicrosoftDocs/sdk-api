---
UID: NF:mixerocx.IMixerOCX.GetStatus
title: IMixerOCX::GetStatus (mixerocx.h)
description: The GetStatus method returns the current status of the Overlay Mixer. (Not implemented.).
helpviewer_keywords: ["GetStatus","GetStatus method [DirectShow]","GetStatus method [DirectShow]","IMixerOCX interface","IMixerOCX interface [DirectShow]","GetStatus method","IMixerOCX.GetStatus","IMixerOCX::GetStatus","IMixerOCXGetStatus","dshow.imixerocx_getstatus","mixerocx/IMixerOCX::GetStatus"]
old-location: dshow\imixerocx_getstatus.htm
tech.root: dshow
ms.assetid: 2be28eec-99cd-4a4e-91fc-77bb51ec6fb3
ms.date: 4/26/2023
ms.keywords: GetStatus, GetStatus method [DirectShow], GetStatus method [DirectShow],IMixerOCX interface, IMixerOCX interface [DirectShow],GetStatus method, IMixerOCX.GetStatus, IMixerOCX::GetStatus, IMixerOCXGetStatus, dshow.imixerocx_getstatus, mixerocx/IMixerOCX::GetStatus
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
 - IMixerOCX::GetStatus
 - mixerocx/IMixerOCX::GetStatus
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
 - IMixerOCX.GetStatus
---

# IMixerOCX::GetStatus


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetStatus</code> method returns the current status of the Overlay Mixer. (Not implemented.)

## -parameters

### -param pdwStatus [out]

Pointer that receives the current status of the Overlay Mixer.

## -returns

Returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>