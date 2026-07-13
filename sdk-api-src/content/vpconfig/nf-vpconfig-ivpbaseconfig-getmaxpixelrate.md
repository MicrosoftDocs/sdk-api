---
UID: NF:vpconfig.IVPBaseConfig.GetMaxPixelRate
title: IVPBaseConfig::GetMaxPixelRate (vpconfig.h)
description: The GetMaxPixelRate method retrieves the maximum pixel rate the device will output for a given width and height.
helpviewer_keywords: ["GetMaxPixelRate","GetMaxPixelRate method [DirectShow]","GetMaxPixelRate method [DirectShow]","IVPBaseConfig interface","IVPBaseConfig interface [DirectShow]","GetMaxPixelRate method","IVPBaseConfig.GetMaxPixelRate","IVPBaseConfig::GetMaxPixelRate","IVPBaseConfigGetMaxPixelRate","dshow.ivpbaseconfig_getmaxpixelrate","vpconfig/IVPBaseConfig::GetMaxPixelRate"]
old-location: dshow\ivpbaseconfig_getmaxpixelrate.htm
tech.root: dshow
ms.assetid: 9b86ff2c-c51f-4498-a000-5f1868c2c24b
ms.date: 4/26/2023
ms.keywords: GetMaxPixelRate, GetMaxPixelRate method [DirectShow], GetMaxPixelRate method [DirectShow],IVPBaseConfig interface, IVPBaseConfig interface [DirectShow],GetMaxPixelRate method, IVPBaseConfig.GetMaxPixelRate, IVPBaseConfig::GetMaxPixelRate, IVPBaseConfigGetMaxPixelRate, dshow.ivpbaseconfig_getmaxpixelrate, vpconfig/IVPBaseConfig::GetMaxPixelRate
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
 - IVPBaseConfig::GetMaxPixelRate
 - vpconfig/IVPBaseConfig::GetMaxPixelRate
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
 - IVPBaseConfig.GetMaxPixelRate
---

# IVPBaseConfig::GetMaxPixelRate


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMaxPixelRate</code> method retrieves the maximum pixel rate the device will output for a given width and height.

## -parameters

### -param pamvpSize [in, out]

Pointer to an <a href="/previous-versions/windows/desktop/api/vptype/ns-vptype-amvpsize">AMVPSIZE</a> structure containing the desired width and height.

### -param pdwMaxPixelsPerSecond [out]

Pointer to a variable that receives the maximum pixel rate, in pixels per second.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method retrieves the maximum pixels per second expected for a given size. If the device does not support this size, then it returns the rate and the size that it supports.

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>