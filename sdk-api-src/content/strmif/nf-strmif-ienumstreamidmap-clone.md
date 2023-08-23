---
UID: NF:strmif.IEnumStreamIdMap.Clone
title: IEnumStreamIdMap::Clone (strmif.h)
description: The Clone method copies the collection.
helpviewer_keywords: ["Clone","Clone method [DirectShow]","Clone method [DirectShow]","IEnumStreamIdMap interface","IEnumStreamIdMap interface [DirectShow]","Clone method","IEnumStreamIdMap.Clone","IEnumStreamIdMap::Clone","IEnumStreamIdMapClone","dshow.ienumstreamidmap_clone","strmif/IEnumStreamIdMap::Clone"]
old-location: dshow\ienumstreamidmap_clone.htm
tech.root: dshow
ms.assetid: 2c6ef2a8-a5d7-434f-8de2-221502b7c5cf
ms.date: 4/26/2023
ms.keywords: Clone, Clone method [DirectShow], Clone method [DirectShow],IEnumStreamIdMap interface, IEnumStreamIdMap interface [DirectShow],Clone method, IEnumStreamIdMap.Clone, IEnumStreamIdMap::Clone, IEnumStreamIdMapClone, dshow.ienumstreamidmap_clone, strmif/IEnumStreamIdMap::Clone
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IEnumStreamIdMap::Clone
 - strmif/IEnumStreamIdMap::Clone
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
 - IEnumStreamIdMap.Clone
---

# IEnumStreamIdMap::Clone


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Clone</code> method copies the collection.

## -parameters

### -param ppIEnumStreamIdMap [out]

Receives a pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ienumstreamidmap">IEnumStreamIdMap</a> interface of the new collection object. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails,an <b>HRESULT</b> error code is returned.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienumstreamidmap">IEnumStreamIdMap Interface</a>