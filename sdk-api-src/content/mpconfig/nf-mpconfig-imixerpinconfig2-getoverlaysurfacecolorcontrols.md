---
UID: NF:mpconfig.IMixerPinConfig2.GetOverlaySurfaceColorControls
title: IMixerPinConfig2::GetOverlaySurfaceColorControls (mpconfig.h)
description: The GetOverlaySurfaceColorControls method retrieves the color control settings associated with the specified overlay surface.
helpviewer_keywords: ["GetOverlaySurfaceColorControls","GetOverlaySurfaceColorControls method [DirectShow]","GetOverlaySurfaceColorControls method [DirectShow]","IMixerPinConfig2 interface","IMixerPinConfig2 interface [DirectShow]","GetOverlaySurfaceColorControls method","IMixerPinConfig2.GetOverlaySurfaceColorControls","IMixerPinConfig2::GetOverlaySurfaceColorControls","IMixerPinConfig2GetOverlaySurfaceColorControls","dshow.imixerpinconfig2_getoverlaysurfacecolorcontrols","mpconfig/IMixerPinConfig2::GetOverlaySurfaceColorControls"]
old-location: dshow\imixerpinconfig2_getoverlaysurfacecolorcontrols.htm
tech.root: dshow
ms.assetid: c6b47e4d-5bf2-4d76-a1e2-88a3342d75a6
ms.date: 4/26/2023
ms.keywords: GetOverlaySurfaceColorControls, GetOverlaySurfaceColorControls method [DirectShow], GetOverlaySurfaceColorControls method [DirectShow],IMixerPinConfig2 interface, IMixerPinConfig2 interface [DirectShow],GetOverlaySurfaceColorControls method, IMixerPinConfig2.GetOverlaySurfaceColorControls, IMixerPinConfig2::GetOverlaySurfaceColorControls, IMixerPinConfig2GetOverlaySurfaceColorControls, dshow.imixerpinconfig2_getoverlaysurfacecolorcontrols, mpconfig/IMixerPinConfig2::GetOverlaySurfaceColorControls
req.header: mpconfig.h
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
 - IMixerPinConfig2::GetOverlaySurfaceColorControls
 - mpconfig/IMixerPinConfig2::GetOverlaySurfaceColorControls
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
 - IMixerPinConfig2.GetOverlaySurfaceColorControls
---

# IMixerPinConfig2::GetOverlaySurfaceColorControls


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetOverlaySurfaceColorControls</code> method retrieves the color control settings associated with the specified overlay surface.

## -parameters

### -param pColorControl [out]

Address of a pointer to the <b>DDCOLORCONTROL</b> structure containing the color values currently applied to the specified surface.

## -returns

Returns an <b>HRESULT</b> value. If the allocator on the pin is not using an overlay surface, the method returns E_FAIL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig2">IMixerPinConfig2 Interface</a>