---
UID: NF:strmif.IResourceConsumer.ReleaseResource
title: IResourceConsumer::ReleaseResource (strmif.h)
description: The ReleaseResource method requests the resource consumer to release the specified resource.
helpviewer_keywords: ["IResourceConsumer interface [DirectShow]","ReleaseResource method","IResourceConsumer.ReleaseResource","IResourceConsumer::ReleaseResource","IResourceConsumerReleaseResource","ReleaseResource","ReleaseResource method [DirectShow]","ReleaseResource method [DirectShow]","IResourceConsumer interface","dshow.iresourceconsumer_releaseresource","strmif/IResourceConsumer::ReleaseResource"]
old-location: dshow\iresourceconsumer_releaseresource.htm
tech.root: dshow
ms.assetid: 9f0a5830-dcaa-4020-9e78-0cbe64e13360
ms.date: 4/26/2023
ms.keywords: IResourceConsumer interface [DirectShow],ReleaseResource method, IResourceConsumer.ReleaseResource, IResourceConsumer::ReleaseResource, IResourceConsumerReleaseResource, ReleaseResource, ReleaseResource method [DirectShow], ReleaseResource method [DirectShow],IResourceConsumer interface, dshow.iresourceconsumer_releaseresource, strmif/IResourceConsumer::ReleaseResource
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
 - IResourceConsumer::ReleaseResource
 - strmif/IResourceConsumer::ReleaseResource
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
 - IResourceConsumer.ReleaseResource
---

# IResourceConsumer::ReleaseResource


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>ReleaseResource</code> method requests the resource consumer to release the specified resource.

## -parameters

### -param idResource [in]

Resource identifier to be released.

## -returns

Returns S_OK if the consumer has released it and requires it again when it becomes available, or S_FALSE if the consumer has not released it but will use <a href="/windows/desktop/api/strmif/nf-strmif-iresourcemanager-notifyrelease">IResourceManager::NotifyRelease</a> when it does.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer Interface</a>