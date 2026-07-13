---
UID: NN:strmif.IResourceConsumer
title: IResourceConsumer (strmif.h)
description: The IResourceConsumer interface provides a callback mechanism for objects using the IResourceManager interface.An object must implement IResourceConsumer if it uses the IResourceManager interface to request resources from the filter graph manager.
helpviewer_keywords: ["IResourceConsumer","IResourceConsumer interface [DirectShow]","IResourceConsumer interface [DirectShow]","described","IResourceConsumerInterface","dshow.iresourceconsumer","strmif/IResourceConsumer"]
old-location: dshow\iresourceconsumer.htm
tech.root: dshow
ms.assetid: dda2b207-dcd8-42df-95a3-d4bfbb4a7fd8
ms.date: 4/26/2023
ms.keywords: IResourceConsumer, IResourceConsumer interface [DirectShow], IResourceConsumer interface [DirectShow],described, IResourceConsumerInterface, dshow.iresourceconsumer, strmif/IResourceConsumer
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
 - IResourceConsumer
 - strmif/IResourceConsumer
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
 - IResourceConsumer
---

# IResourceConsumer interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IResourceConsumer</code> interface provides a callback mechanism for objects using the <a href="/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager</a> interface.

An object must implement <code>IResourceConsumer</code> if it uses the <a href="/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager</a> interface to request resources from the filter graph manager. The filter graph manager calls methods on <code>IResourceConsumer</code> to notify the object when a resource becomes available, or when the object should release a resource that it acquired.

Applications typically do not use or implement this interface.

## -inheritance

The <b>IResourceConsumer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResourceConsumer</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager Interface</a>
