---
UID: NF:mpconfig.IMixerPinConfig.SetZOrder
title: IMixerPinConfig::SetZOrder (mpconfig.h)
description: The SetZOrder method sets the z-order of a particular video stream.
helpviewer_keywords: ["IMixerPinConfig interface [DirectShow]","SetZOrder method","IMixerPinConfig.SetZOrder","IMixerPinConfig::SetZOrder","IMixerPinConfigSetZOrder","SetZOrder","SetZOrder method [DirectShow]","SetZOrder method [DirectShow]","IMixerPinConfig interface","dshow.imixerpinconfig_setzorder","mpconfig/IMixerPinConfig::SetZOrder"]
old-location: dshow\imixerpinconfig_setzorder.htm
tech.root: dshow
ms.assetid: fe8e71b8-9aaf-438e-b370-5ba9f131bf7a
ms.date: 4/26/2023
ms.keywords: IMixerPinConfig interface [DirectShow],SetZOrder method, IMixerPinConfig.SetZOrder, IMixerPinConfig::SetZOrder, IMixerPinConfigSetZOrder, SetZOrder, SetZOrder method [DirectShow], SetZOrder method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setzorder, mpconfig/IMixerPinConfig::SetZOrder
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
 - IMixerPinConfig::SetZOrder
 - mpconfig/IMixerPinConfig::SetZOrder
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
 - IMixerPinConfig.SetZOrder
---

# IMixerPinConfig::SetZOrder


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetZOrder</code> method sets the z-order of a particular video stream.



This method is not currently implemented and returns E_NOTIMPL.

## -parameters

### -param dwZOrder [in]

Value indicating the order in which streams will clip each other.

## -returns

Returns E_NOTIMPL.

## -remarks

The z-order indicates which streams can clip other streams. Images with larger z-values are always in front of images with smaller z-values.

The relative order of multiple streams is significant only if the video images overlap.

Specifying the same z-order for two overlapping streams can cause strange video artifacts.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getzorder">IMixerPinConfig::GetZOrder</a>