---
UID: NN:strmif.IQualityControl
title: IQualityControl (strmif.h)
description: The IQualityControl interface provides support for quality control.
helpviewer_keywords: ["IQualityControl","IQualityControl interface [DirectShow]","IQualityControl interface [DirectShow]","described","IQualityControlInterface","dshow.iqualitycontrol","strmif/IQualityControl"]
old-location: dshow\iqualitycontrol.htm
tech.root: dshow
ms.assetid: 2672e563-75d7-4a8a-b914-7b0712e856e8
ms.date: 4/26/2023
ms.keywords: IQualityControl, IQualityControl interface [DirectShow], IQualityControl interface [DirectShow],described, IQualityControlInterface, dshow.iqualitycontrol, strmif/IQualityControl
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
 - IQualityControl
 - strmif/IQualityControl
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
 - IQualityControl
---

# IQualityControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IQualityControl</code> interface provides support for quality control. An object exposes this interface if it can generate or receive quality-control messages. This includes renderer filters (which typically generate quality control messages), pins (which receive them), and external quality managers (which also receive them).

A renderer filter generates a quality-control message by calling the <a href="/windows/desktop/api/strmif/nf-strmif-iqualitycontrol-notify">IQualityControl::Notify</a> method on the output pin of the upstream filter. The upstream filter either handles the message or passes it upstream.

An application can implement its own quality-control manager. Call <a href="/windows/desktop/api/strmif/nf-strmif-iqualitycontrol-setsink">IQualityControl::SetSink</a> on the renderer to designate the quality-control manager as the recipient for quality-control messages. Calling this method overrides the default handling of quality-control messages.

However, most applications will not implement their own quality-control managers; and aside from this special case, applications typically do not use this interface. For more information, see <a href="/windows/desktop/DirectShow/quality-control-management">Quality-Control Management</a>

## -inheritance

The <b>IQualityControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQualityControl</b> also has these types of members:

