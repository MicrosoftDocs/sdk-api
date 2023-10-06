---
UID: NF:vpconfig.IVPConfig.IsVPDecimationAllowed
title: IVPConfig::IsVPDecimationAllowed (vpconfig.h)
description: The IsVPDecimationAllowed method, given the context, retrieves whether scaling at the video port is possible.
helpviewer_keywords: ["IVPConfig interface [DirectShow]","IsVPDecimationAllowed method","IVPConfig.IsVPDecimationAllowed","IVPConfig::IsVPDecimationAllowed","IVPConfigIsVPDecimationAllowed","IsVPDecimationAllowed","IsVPDecimationAllowed method [DirectShow]","IsVPDecimationAllowed method [DirectShow]","IVPConfig interface","dshow.ivpconfig_isvpdecimationallowed","vpconfig/IVPConfig::IsVPDecimationAllowed"]
old-location: dshow\ivpconfig_isvpdecimationallowed.htm
tech.root: dshow
ms.assetid: 2362e321-cbdd-41ee-97ff-e6ff9cd672b0
ms.date: 4/26/2023
ms.keywords: IVPConfig interface [DirectShow],IsVPDecimationAllowed method, IVPConfig.IsVPDecimationAllowed, IVPConfig::IsVPDecimationAllowed, IVPConfigIsVPDecimationAllowed, IsVPDecimationAllowed, IsVPDecimationAllowed method [DirectShow], IsVPDecimationAllowed method [DirectShow],IVPConfig interface, dshow.ivpconfig_isvpdecimationallowed, vpconfig/IVPConfig::IsVPDecimationAllowed
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVPConfig::IsVPDecimationAllowed
 - vpconfig/IVPConfig::IsVPDecimationAllowed
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
 - IVPConfig.IsVPDecimationAllowed
---

# IVPConfig::IsVPDecimationAllowed


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsVPDecimationAllowed</code> method, given the context, retrieves whether scaling at the video port is possible.

## -parameters

### -param pbIsDecimationAllowed [out]

Receives a Boolean value indicating whether decimation is possible.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

The <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter uses this function to determine whether the driver needs the mixer to decimate video data at its own discretion. This function can be especially useful in a capture with preview situation in which you would not want the VP mixer filter to perform any scaling at the video port.

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig">IVPConfig Interface</a>