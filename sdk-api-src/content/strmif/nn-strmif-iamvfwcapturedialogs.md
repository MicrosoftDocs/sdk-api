---
UID: NN:strmif.IAMVfwCaptureDialogs
title: IAMVfwCaptureDialogs (strmif.h)
description: The IAMVfwCaptureDialogs interface displays a dialog box provided by a Video for Windows (VFW) capture driver.The VFW Capture filter implements this interface.
helpviewer_keywords: ["IAMVfwCaptureDialogs","IAMVfwCaptureDialogs interface [DirectShow]","IAMVfwCaptureDialogs interface [DirectShow]","described","IAMVfwCaptureDialogsInterface","dshow.iamvfwcapturedialogs","strmif/IAMVfwCaptureDialogs"]
old-location: dshow\iamvfwcapturedialogs.htm
tech.root: dshow
ms.assetid: 5198c80c-28f3-4b5c-9b3b-aa502bf3a384
ms.date: 4/26/2023
ms.keywords: IAMVfwCaptureDialogs, IAMVfwCaptureDialogs interface [DirectShow], IAMVfwCaptureDialogs interface [DirectShow],described, IAMVfwCaptureDialogsInterface, dshow.iamvfwcapturedialogs, strmif/IAMVfwCaptureDialogs
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
 - IAMVfwCaptureDialogs
 - strmif/IAMVfwCaptureDialogs
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
 - IAMVfwCaptureDialogs
---

# IAMVfwCaptureDialogs interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMVfwCaptureDialogs</code> interface displays a dialog box provided by a Video for Windows (VFW) capture driver.

The <a href="/windows/desktop/DirectShow/vfw-capture-filter">VFW Capture</a> filter implements this interface. Applications can use it to display one of the three dialog boxes (Source, Format, or Display) provided by VFW capture drivers.

## -inheritance

The <b>IAMVfwCaptureDialogs</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMVfwCaptureDialogs</b> also has these types of members:

