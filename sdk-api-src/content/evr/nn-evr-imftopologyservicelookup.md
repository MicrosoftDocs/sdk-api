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

Enables a custom video mixer or video presenter to get interface pointers from the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR). The mixer can also use this interface to get interface pointers from the presenter, and the presenter can use it to get interface pointers from the mixer.

To use this interface, implement the <a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient">IMFTopologyServiceLookupClient</a> interface on your custom mixer or presenter. The EVR calls <a href="/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers">IMFTopologyServiceLookupClient::InitServicePointers</a> with a pointer to the EVR's <b>IMFTopologyServiceLookup</b> interface.

## -inheritance

The <b>IMFTopologyServiceLookup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTopologyServiceLookup</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
