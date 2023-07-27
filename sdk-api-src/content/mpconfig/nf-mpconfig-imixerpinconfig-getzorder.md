---
UID: NF:mpconfig.IMixerPinConfig.GetZOrder
title: IMixerPinConfig::GetZOrder (mpconfig.h)
description: The GetZOrder method retrieves the z-order of a particular video stream.
helpviewer_keywords: ["GetZOrder","GetZOrder method [DirectShow]","GetZOrder method [DirectShow]","IMixerPinConfig interface","IMixerPinConfig interface [DirectShow]","GetZOrder method","IMixerPinConfig.GetZOrder","IMixerPinConfig::GetZOrder","IMixerPinConfigGetZOrder","dshow.imixerpinconfig_getzorder","mpconfig/IMixerPinConfig::GetZOrder"]
old-location: dshow\imixerpinconfig_getzorder.htm
tech.root: dshow
ms.assetid: 5089a2b3-2973-4761-82f6-f6af3ac9f560
ms.date: 4/26/2023
ms.keywords: GetZOrder, GetZOrder method [DirectShow], GetZOrder method [DirectShow],IMixerPinConfig interface, IMixerPinConfig interface [DirectShow],GetZOrder method, IMixerPinConfig.GetZOrder, IMixerPinConfig::GetZOrder, IMixerPinConfigGetZOrder, dshow.imixerpinconfig_getzorder, mpconfig/IMixerPinConfig::GetZOrder
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
 - IMixerPinConfig::GetZOrder
 - mpconfig/IMixerPinConfig::GetZOrder
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
 - IMixerPinConfig.GetZOrder
---

# IMixerPinConfig::GetZOrder


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetZOrder</code> method retrieves the z-order of a particular video stream.



This method is not currently implemented and returns E_NOTIMPL.

## -parameters

### -param pdwZOrder [out]

Pointer to a value indicating the order in which streams will clip each other.

## -returns

Returns E_NOTIMPL.

## -remarks

Images with larger z-values are always in front of images with smaller z-values.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setzorder">IMixerPinConfig::SetZOrder</a>