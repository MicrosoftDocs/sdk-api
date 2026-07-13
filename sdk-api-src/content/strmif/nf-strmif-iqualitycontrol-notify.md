---
UID: NF:strmif.IQualityControl.Notify
title: IQualityControl::Notify (strmif.h)
description: The Notify method notifies the filter that a quality change is requested.
helpviewer_keywords: ["IQualityControl interface [DirectShow]","Notify method","IQualityControl.Notify","IQualityControl::Notify","IQualityControlNotify","Notify","Notify method [DirectShow]","Notify method [DirectShow]","IQualityControl interface","dshow.iqualitycontrol_notify","strmif/IQualityControl::Notify"]
old-location: dshow\iqualitycontrol_notify.htm
tech.root: dshow
ms.assetid: c7a34356-b0b2-49c1-bdc2-d8043fdc2862
ms.date: 4/26/2023
ms.keywords: IQualityControl interface [DirectShow],Notify method, IQualityControl.Notify, IQualityControl::Notify, IQualityControlNotify, Notify, Notify method [DirectShow], Notify method [DirectShow],IQualityControl interface, dshow.iqualitycontrol_notify, strmif/IQualityControl::Notify
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
 - IQualityControl::Notify
 - strmif/IQualityControl::Notify
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
 - IQualityControl.Notify
---

# IQualityControl::Notify


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Notify</code> method notifies the filter that a quality change is requested.

## -parameters

### -param pSelf [in]

Pointer to the filter that is sending the quality notification.

### -param q [in]

[Quality](/windows/desktop/api/strmif/ns-strmif-quality) structure.

## -returns

Returns S_OK if the method succeeds; otherwise, returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iqualitycontrol">IQualityControl Interface</a>