---
UID: NF:vpconfig.IVPConfig.SetScalingFactors
title: IVPConfig::SetScalingFactors (vpconfig.h)
description: The SetScalingFactors method sets the factors by which the decoder should scale the video stream.
helpviewer_keywords: ["IVPConfig interface [DirectShow]","SetScalingFactors method","IVPConfig.SetScalingFactors","IVPConfig::SetScalingFactors","IVPConfigSetScalingFactors","SetScalingFactors","SetScalingFactors method [DirectShow]","SetScalingFactors method [DirectShow]","IVPConfig interface","dshow.ivpconfig_setscalingfactors","vpconfig/IVPConfig::SetScalingFactors"]
old-location: dshow\ivpconfig_setscalingfactors.htm
tech.root: dshow
ms.assetid: 62b8281e-6feb-43f5-b1a5-36444fda5543
ms.date: 4/26/2023
ms.keywords: IVPConfig interface [DirectShow],SetScalingFactors method, IVPConfig.SetScalingFactors, IVPConfig::SetScalingFactors, IVPConfigSetScalingFactors, SetScalingFactors, SetScalingFactors method [DirectShow], SetScalingFactors method [DirectShow],IVPConfig interface, dshow.ivpconfig_setscalingfactors, vpconfig/IVPConfig::SetScalingFactors
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
 - IVPConfig::SetScalingFactors
 - vpconfig/IVPConfig::SetScalingFactors
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
 - IVPConfig.SetScalingFactors
---

# IVPConfig::SetScalingFactors


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetScalingFactors</code> method sets the factors by which the decoder should scale the video stream.

## -parameters

### -param pamvpSize [in]

Pointer to the new scaling size structure (<a href="/previous-versions/windows/desktop/api/vptype/ns-vptype-amvpsize">AMVPSIZE</a>) to use to specify the width and height.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

If the decoder does not support the specified scaling factors, then it sets the values to the nearest factors it can support.

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig">IVPConfig Interface</a>