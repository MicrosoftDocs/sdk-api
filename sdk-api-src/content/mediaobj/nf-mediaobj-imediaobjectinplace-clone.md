---
UID: NF:mediaobj.IMediaObjectInPlace.Clone
title: IMediaObjectInPlace::Clone (mediaobj.h)
description: The Clone method creates a copy of the DMO in its current state.
helpviewer_keywords: ["Clone","Clone method [DirectShow]","Clone method [DirectShow]","IMediaObjectInPlace interface","IMediaObjectInPlace interface [DirectShow]","Clone method","IMediaObjectInPlace.Clone","IMediaObjectInPlace::Clone","IMediaObjectInPlaceClone","dshow.imediaobjectinplace_clone","mediaobj/IMediaObjectInPlace::Clone"]
old-location: dshow\imediaobjectinplace_clone.htm
tech.root: dshow
ms.assetid: 6660afa8-3502-4e88-925b-192e06346243
ms.date: 4/26/2023
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IMediaObjectInPlace interface, IMediaObjectInPlace interface [DirectShow],Clone method, IMediaObjectInPlace.Clone, IMediaObjectInPlace::Clone, IMediaObjectInPlaceClone, dshow.imediaobjectinplace_clone, mediaobj/IMediaObjectInPlace::Clone
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
 - IMediaObjectInPlace::Clone
 - mediaobj/IMediaObjectInPlace::Clone
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
 - IMediaObjectInPlace.Clone
---

# IMediaObjectInPlace::Clone


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Clone</code> method creates a copy of the DMO in its current state.

## -parameters

### -param ppMediaObject [out]

Address of a pointer to receive the new DMO's <a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace">IMediaObjectInPlace</a> interface.

## -returns

Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

If the method succeeds, the <b>IMediaObjectInPlace</b> interface that it returns has an outstanding reference count. Be sure to release the interface when you are finished using it.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace">IMediaObjectInPlace Interface</a>