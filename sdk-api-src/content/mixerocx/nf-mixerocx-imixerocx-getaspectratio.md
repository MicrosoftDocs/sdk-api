---
UID: NF:mixerocx.IMixerOCX.GetAspectRatio
title: IMixerOCX::GetAspectRatio (mixerocx.h)
description: The GetAspectRatio method returns the current aspect ratio setting on the Overlay Mixer. (Currently not implemented.).
helpviewer_keywords: ["GetAspectRatio","GetAspectRatio method [DirectShow]","GetAspectRatio method [DirectShow]","IMixerOCX interface","IMixerOCX interface [DirectShow]","GetAspectRatio method","IMixerOCX.GetAspectRatio","IMixerOCX::GetAspectRatio","IMixerOCXGetAspectRatio","dshow.imixerocx_getaspectratio","mixerocx/IMixerOCX::GetAspectRatio"]
old-location: dshow\imixerocx_getaspectratio.htm
tech.root: dshow
ms.assetid: 6143ba3c-6472-47d3-b3ca-55c06ca8da0e
ms.date: 4/26/2023
ms.keywords: GetAspectRatio, GetAspectRatio method [DirectShow], GetAspectRatio method [DirectShow],IMixerOCX interface, IMixerOCX interface [DirectShow],GetAspectRatio method, IMixerOCX.GetAspectRatio, IMixerOCX::GetAspectRatio, IMixerOCXGetAspectRatio, dshow.imixerocx_getaspectratio, mixerocx/IMixerOCX::GetAspectRatio
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
 - IMixerOCX::GetAspectRatio
 - mixerocx/IMixerOCX::GetAspectRatio
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
 - IMixerOCX.GetAspectRatio
---

# IMixerOCX::GetAspectRatio


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetAspectRatio</code> method returns the current aspect ratio setting on the Overlay Mixer. (Currently not implemented.)

## -parameters

### -param pdwPictAspectRatioX [out]

Pointer that receives the value of the X dimension.

### -param pdwPictAspectRatioY [out]

Pointer that receives the value of the Y dimension.

## -returns

Returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>