---
UID: NF:strmif.IAMVideoControl.GetCaps
title: IAMVideoControl::GetCaps (strmif.h)
description: The GetCaps method retrieves the capabilities of the underlying hardware.
helpviewer_keywords: ["GetCaps","GetCaps method [DirectShow]","GetCaps method [DirectShow]","IAMVideoControl interface","IAMVideoControl interface [DirectShow]","GetCaps method","IAMVideoControl.GetCaps","IAMVideoControl::GetCaps","IAMVideoControlGetCaps","dshow.iamvideocontrol_getcaps","strmif/IAMVideoControl::GetCaps"]
old-location: dshow\iamvideocontrol_getcaps.htm
tech.root: dshow
ms.assetid: 8e4b7b46-8179-410c-8369-652f9b65de8c
ms.date: 4/26/2023
ms.keywords: GetCaps, GetCaps method [DirectShow], GetCaps method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetCaps method, IAMVideoControl.GetCaps, IAMVideoControl::GetCaps, IAMVideoControlGetCaps, dshow.iamvideocontrol_getcaps, strmif/IAMVideoControl::GetCaps
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMVideoControl::GetCaps
 - strmif/IAMVideoControl::GetCaps
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
 - IAMVideoControl.GetCaps
---

# IAMVideoControl::GetCaps


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCaps</code> method retrieves the capabilities of the underlying hardware.

## -parameters

### -param pPin [in]

Pointer to the pin to query capabilities from.

### -param pCapsFlags [out]

Pointer to a value representing a combination of the flags from the [VideoControlFlags](/windows/desktop/api/strmif/ne-strmif-videocontrolflags) enumeration.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

Possible capabilities include one or more of the following: flipping the picture horizontally, flipping the picture vertically, enabling external triggers, and simulating external triggers.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocontrol">IAMVideoControl Interface</a>