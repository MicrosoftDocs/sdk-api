---
UID: NF:mediaobj.IMediaObject.FreeStreamingResources
title: IMediaObject::FreeStreamingResources (mediaobj.h)
description: The FreeStreamingResources method frees resources allocated by the DMO. Calling this method is always optional.
helpviewer_keywords: ["FreeStreamingResources","FreeStreamingResources method [DirectShow]","FreeStreamingResources method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","FreeStreamingResources method","IMediaObject.FreeStreamingResources","IMediaObject::FreeStreamingResources","IMediaObjectFreeStreamingResources","dshow.imediaobject_freestreamingresources","mediaobj/IMediaObject::FreeStreamingResources"]
old-location: dshow\imediaobject_freestreamingresources.htm
tech.root: dshow
ms.assetid: c4d2dbf1-45c9-47a2-a21f-5eb04f828ec1
ms.date: 4/26/2023
ms.keywords: FreeStreamingResources, FreeStreamingResources method [DirectShow], FreeStreamingResources method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],FreeStreamingResources method, IMediaObject.FreeStreamingResources, IMediaObject::FreeStreamingResources, IMediaObjectFreeStreamingResources, dshow.imediaobject_freestreamingresources, mediaobj/IMediaObject::FreeStreamingResources
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObject::FreeStreamingResources
 - mediaobj/IMediaObject::FreeStreamingResources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.FreeStreamingResources
---

# IMediaObject::FreeStreamingResources


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>FreeStreamingResources</code> method frees resources allocated by the DMO. Calling this method is always optional.



## -returns

Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

This method releases any resources that the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources">IMediaObject::AllocateStreamingResources</a> method initializes.

If the DMO does not support this method, the method returns S_OK. If you call this method during streaming, the method fails and the DMO does not release any resources.

Regardless of whether the method fails or succeeds, the application can continue to call other methods on the DMO. The DMO might need to re-initialize resources that were previously freed.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>
