---
UID: NF:strmif.IAMVideoControl.GetMode
title: IAMVideoControl::GetMode (strmif.h)
description: The GetMode method retrieves the video control mode of operation.
helpviewer_keywords: ["GetMode","GetMode method [DirectShow]","GetMode method [DirectShow]","IAMVideoControl interface","IAMVideoControl interface [DirectShow]","GetMode method","IAMVideoControl.GetMode","IAMVideoControl::GetMode","IAMVideoControlGetMode","dshow.iamvideocontrol_getmode","strmif/IAMVideoControl::GetMode"]
old-location: dshow\iamvideocontrol_getmode.htm
tech.root: dshow
ms.assetid: 4b937661-67b2-445c-ab25-8655e1036797
ms.date: 4/26/2023
ms.keywords: GetMode, GetMode method [DirectShow], GetMode method [DirectShow],IAMVideoControl interface, IAMVideoControl interface [DirectShow],GetMode method, IAMVideoControl.GetMode, IAMVideoControl::GetMode, IAMVideoControlGetMode, dshow.iamvideocontrol_getmode, strmif/IAMVideoControl::GetMode
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
 - IAMVideoControl::GetMode
 - strmif/IAMVideoControl::GetMode
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
 - IAMVideoControl.GetMode
---

# IAMVideoControl::GetMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMode</code> method retrieves the video control mode of operation.

## -parameters

### -param pPin [in]

Pointer to the pin to retrieve the video control mode from.

### -param Mode [out]

Pointer to a value representing a combination of the flags from the [VideoControlFlags](/windows/desktop/api/strmif/ne-strmif-videocontrolflags) enumeration, which specify the video control mode.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

Possible modes of operation include one or more of the following: flipping the picture horizontally, flipping the picture vertically, enabling external triggers, and simulating external triggers.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideocontrol">IAMVideoControl Interface</a>