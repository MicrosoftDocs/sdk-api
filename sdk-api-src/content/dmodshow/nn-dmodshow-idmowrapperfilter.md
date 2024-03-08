---
UID: NN:dmodshow.IDMOWrapperFilter
title: IDMOWrapperFilter (dmodshow.h)
description: The IDMOWrapperFilter interface enables an application to use a DirectX Media Object (DMO) inside a filter graph.
helpviewer_keywords: ["IDMOWrapperFilter","IDMOWrapperFilter interface [DirectShow]","IDMOWrapperFilter interface [DirectShow]","described","IDMOWrapperFilterInterface","dmodshow/IDMOWrapperFilter","dshow.idmowrapperfilter"]
old-location: dshow\idmowrapperfilter.htm
tech.root: dshow
ms.assetid: c85b828c-095d-4991-85a8-65b96529f305
ms.date: 4/26/2023
ms.keywords: IDMOWrapperFilter, IDMOWrapperFilter interface [DirectShow], IDMOWrapperFilter interface [DirectShow],described, IDMOWrapperFilterInterface, dmodshow/IDMOWrapperFilter, dshow.idmowrapperfilter
req.header: dmodshow.h
req.include-header: 
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMOWrapperFilter
 - dmodshow/IDMOWrapperFilter
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
 - IDMOWrapperFilter
---

# IDMOWrapperFilter interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDMOWrapperFilter</code> interface enables an application to use a DirectX Media Object (DMO) inside a filter graph. The <a href="/windows/desktop/DirectShow/dmo-wrapper-filter">DMO Wrapper</a> filter exposes this interface.

To add a DMO to the filter graph, create an instance of the DMO Wrapper filter and query it for the <code>IDMOWrapperFilter</code> interface. Then call the <a href="/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init">IDMOWrapperFilter::Init</a> method to initialize the filter with the DMO.

## -inheritance

The <b>IDMOWrapperFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDMOWrapperFilter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/directx-media-objects">DirectX Media Objects</a>
