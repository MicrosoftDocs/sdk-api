---
UID: NN:control.IBasicVideo
title: IBasicVideo (control.h)
description: The IBasicVideo interface sets video properties such as the destination and source rectangles.
helpviewer_keywords: ["IBasicVideo","IBasicVideo interface [DirectShow]","IBasicVideo interface [DirectShow]","described","IBasicVideoInterface","control/IBasicVideo","dshow.ibasicvideo"]
old-location: dshow\ibasicvideo.htm
tech.root: dshow
ms.assetid: 14f45bdc-2271-459d-b165-c860c8fc3e0b
ms.date: 4/26/2023
ms.keywords: IBasicVideo, IBasicVideo interface [DirectShow], IBasicVideo interface [DirectShow],described, IBasicVideoInterface, control/IBasicVideo, dshow.ibasicvideo
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
 - IBasicVideo
 - control/IBasicVideo
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
 - IBasicVideo
---

# IBasicVideo interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IBasicVideo</code> interface sets video properties such as the destination and source rectangles. The <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter and Video Mixing Renderer filters implement this interface, but the interface is exposed to applications through the Filter Graph Manager. Applications should always retrieve this interface from the Filter Graph Manager.

The <code>IBasicVideo</code> interface manipulates the following rectangles associated with the video image:

<ul>
<li>The <i>source</i> rectangle is the portion of the original image that gets displayed.</li>
<li>The <i>destination</i> rectangle is the portion of the video window the receives the source rectangle.</li>
<li>The <i>video</i> rectangle is the original video image.</li>
</ul>
In other words, the video renderer crops the image to the source rectangle, and then stretches or shrinks the cropped image to the destination rectangle. All rectangle dimensions are given in pixels.

Properties set on the Video Renderer persist between successive connections and disconnections.

<b>Error codes</b>: If the video renderer filter is not connected to another filter, all methods return the error code VFW_E_NOT_CONNECTED. For the Filter Graph Manager's implementation, if the graph does not contain a video renderer filter, all methods return E_NOINTERFACE. Note that the Filter Graph Manager exposes the interface even when the graph does not contain a video renderer, so an application can query for the interface before it builds the graph.

## -inheritance

The <b>IBasicVideo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IBasicVideo</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
