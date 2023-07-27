---
UID: NF:control.IBasicVideo.IsUsingDefaultSource
title: IBasicVideo::IsUsingDefaultSource (control.h)
description: The IsUsingDefaultSource method queries whether the renderer is using the default source rectangle.
helpviewer_keywords: ["IBasicVideo interface [DirectShow]","IsUsingDefaultSource method","IBasicVideo.IsUsingDefaultSource","IBasicVideo::IsUsingDefaultSource","IBasicVideoIsUsingDefaultSource","IsUsingDefaultSource","IsUsingDefaultSource method [DirectShow]","IsUsingDefaultSource method [DirectShow]","IBasicVideo interface","control/IBasicVideo::IsUsingDefaultSource","dshow.ibasicvideo_isusingdefaultsource"]
old-location: dshow\ibasicvideo_isusingdefaultsource.htm
tech.root: dshow
ms.assetid: 85cb633f-95cd-4cbe-9572-324ec784e6bb
ms.date: 4/26/2023
ms.keywords: IBasicVideo interface [DirectShow],IsUsingDefaultSource method, IBasicVideo.IsUsingDefaultSource, IBasicVideo::IsUsingDefaultSource, IBasicVideoIsUsingDefaultSource, IsUsingDefaultSource, IsUsingDefaultSource method [DirectShow], IsUsingDefaultSource method [DirectShow],IBasicVideo interface, control/IBasicVideo::IsUsingDefaultSource, dshow.ibasicvideo_isusingdefaultsource
req.header: control.h
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
 - IBasicVideo::IsUsingDefaultSource
 - control/IBasicVideo::IsUsingDefaultSource
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
 - IBasicVideo.IsUsingDefaultSource
---

# IBasicVideo::IsUsingDefaultSource


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsUsingDefaultSource</code> method queries whether the renderer is using the default source rectangle.



## -returns

Returns S_OK if the renderer is using the default source rectangle, or S_FALSE otherwise.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>



<a href="/windows/desktop/api/control/nf-control-ibasicvideo-setdefaultsourceposition">IBasicVideo::SetDefaultSourcePosition</a>
