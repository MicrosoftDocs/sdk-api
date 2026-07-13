---
UID: NN:mediaobj.IDMOQualityControl
title: IDMOQualityControl (mediaobj.h)
description: The IDMOQualityControl interface supports quality control on a Microsoft DirectX Media Object (DMO).
helpviewer_keywords: ["IDMOQualityControl","IDMOQualityControl interface [DirectShow]","IDMOQualityControl interface [DirectShow]","described","IDMOQualityControlInterface","dshow.idmoqualitycontrol","mediaobj/IDMOQualityControl"]
old-location: dshow\idmoqualitycontrol.htm
tech.root: dshow
ms.assetid: c23211f2-d4ba-45ff-b443-3425c3a3e72f
ms.date: 4/26/2023
ms.keywords: IDMOQualityControl, IDMOQualityControl interface [DirectShow], IDMOQualityControl interface [DirectShow],described, IDMOQualityControlInterface, dshow.idmoqualitycontrol, mediaobj/IDMOQualityControl
req.header: mediaobj.h
req.include-header: Dmoguids.lib
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDMOQualityControl
 - mediaobj/IDMOQualityControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mediaobj.h
api_name:
 - IDMOQualityControl
---

# IDMOQualityControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDMOQualityControl</code> interface supports quality control on a Microsoft DirectX Media Object (DMO).



A DMO exposes this interface if it can respond to late samples. When quality control is enabled, the DMO attempts to process samples on time, discarding late samples if necessary. When quality control is disabled, the DMO processes every sample. By default, quality control is disabled.

Applications use this interface to enable or disable quality control. Using quality control is appropriate when you are viewing media data in real time. If you are capturing data to a file, do not enable quality control, because the DMO might discard samples. It does not matter in file capture whether samples arrive late, and you do not want to lose the data.

To use quality control, perform the following steps:
<ol>
<li>Call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-idmoqualitycontrol-setnow">IDMOQualityControl::SetNow</a> method with the reference time of the earliest sample to be processed.</li>
<li>Call the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-idmoqualitycontrol-setstatus">IDMOQualityControl::SetStatus</a> method with the DMO_QUALITY_STATUS_ENABLED flag.</li>
</ol>To disable quality control, call <b>SetStatus</b> with no flag.

## -inheritance

The <b>IDMOQualityControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDMOQualityControl</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

