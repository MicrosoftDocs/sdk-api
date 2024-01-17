---
UID: NN:evr.IMFTopologyServiceLookup
title: IMFTopologyServiceLookup (evr.h)
description: Enables a custom video mixer or video presenter to get interface pointers from the Enhanced Video Renderer (EVR).
helpviewer_keywords: ["IMFTopologyServiceLookup","IMFTopologyServiceLookup interface [Media Foundation]","IMFTopologyServiceLookup interface [Media Foundation]","described","a912c17a-40ef-441c-bfc9-7ef49d22070f","evr/IMFTopologyServiceLookup","mf.imftopologyservicelookup"]
old-location: mf\imftopologyservicelookup.htm
tech.root: mfarchive
ms.assetid: a912c17a-40ef-441c-bfc9-7ef49d22070f
ms.date: 12/05/2018
ms.keywords: IMFTopologyServiceLookup, IMFTopologyServiceLookup interface [Media Foundation], IMFTopologyServiceLookup interface [Media Foundation],described, a912c17a-40ef-441c-bfc9-7ef49d22070f, evr/IMFTopologyServiceLookup, mf.imftopologyservicelookup
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IMFTopologyServiceLookup
 - evr/IMFTopologyServiceLookup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFTopologyServiceLookup
archived: true
---

# IMFTopologyServiceLookup interface


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Enables a custom video mixer or video presenter to get interface pointers from the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR). The mixer can also use this interface to get interface pointers from the presenter, and the presenter can use it to get interface pointers from the mixer.

To use this interface, implement the <a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient">IMFTopologyServiceLookupClient</a> interface on your custom mixer or presenter. The EVR calls <a href="/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers">IMFTopologyServiceLookupClient::InitServicePointers</a> with a pointer to the EVR's <b>IMFTopologyServiceLookup</b> interface.

## -inheritance

The <b>IMFTopologyServiceLookup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTopologyServiceLookup</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
