---
UID: NF:vpconfig.IVPBaseConfig.SetSurfaceParameters
title: IVPBaseConfig::SetSurfaceParameters (vpconfig.h)
description: The SetSurfaceParameters method informs the device of the layout of the overlay surface. The downstream filter (the Overlay Mixer, VBI Surface Allocator, or Video Port Manager) calls this method after it creates the overlay surface.
helpviewer_keywords: ["IVPBaseConfig interface [DirectShow]","SetSurfaceParameters method","IVPBaseConfig.SetSurfaceParameters","IVPBaseConfig::SetSurfaceParameters","IVPBaseConfigSetSurfaceParameters","SetSurfaceParameters","SetSurfaceParameters method [DirectShow]","SetSurfaceParameters method [DirectShow]","IVPBaseConfig interface","dshow.ivpbaseconfig_setsurfaceparameters","vpconfig/IVPBaseConfig::SetSurfaceParameters"]
old-location: dshow\ivpbaseconfig_setsurfaceparameters.htm
tech.root: dshow
ms.assetid: 4af0092e-5866-45ca-b0be-e97d9dd51b0f
ms.date: 4/26/2023
ms.keywords: IVPBaseConfig interface [DirectShow],SetSurfaceParameters method, IVPBaseConfig.SetSurfaceParameters, IVPBaseConfig::SetSurfaceParameters, IVPBaseConfigSetSurfaceParameters, SetSurfaceParameters, SetSurfaceParameters method [DirectShow], SetSurfaceParameters method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setsurfaceparameters, vpconfig/IVPBaseConfig::SetSurfaceParameters
req.header: vpconfig.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVPBaseConfig::SetSurfaceParameters
 - vpconfig/IVPBaseConfig::SetSurfaceParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.SetSurfaceParameters
---

# IVPBaseConfig::SetSurfaceParameters


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetSurfaceParameters</code> method informs the device of the layout of the overlay surface. The downstream filter (the Overlay Mixer, VBI Surface Allocator, or Video Port Manager) calls this method after it creates the overlay surface.

## -parameters

### -param dwPitch [in]

Specifies the stride of the surface (also called the <i>pitch</i>), in pixels.

### -param dwXOrigin [in]

Specifies the X-coordinate of the pixel at which valid data starts.

### -param dwYOrigin [in]

Specifies the Y-coordinate of the pixel at which valid data starts.

## -returns

Returns S_OK if successful, or E_NOTIMPL.

## -remarks

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>