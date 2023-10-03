---
UID: NN:evr.IMFTopologyServiceLookupClient
title: IMFTopologyServiceLookupClient (evr.h)
description: Initializes a video mixer or presenter.
helpviewer_keywords: ["IMFTopologyServiceLookupClient","IMFTopologyServiceLookupClient interface [Media Foundation]","IMFTopologyServiceLookupClient interface [Media Foundation]","described","c4215d08-3734-44b9-b053-0d49d89a90f6","evr/IMFTopologyServiceLookupClient","mf.imftopologyservicelookupclient"]
old-location: mf\imftopologyservicelookupclient.htm
tech.root: mfarchive
ms.assetid: c4215d08-3734-44b9-b053-0d49d89a90f6
ms.date: 12/05/2018
ms.keywords: IMFTopologyServiceLookupClient, IMFTopologyServiceLookupClient interface [Media Foundation], IMFTopologyServiceLookupClient interface [Media Foundation],described, c4215d08-3734-44b9-b053-0d49d89a90f6, evr/IMFTopologyServiceLookupClient, mf.imftopologyservicelookupclient
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
 - IMFTopologyServiceLookupClient
 - evr/IMFTopologyServiceLookupClient
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
 - IMFTopologyServiceLookupClient
archived: true
---

# IMFTopologyServiceLookupClient interface


## -description

Initializes a video mixer or presenter. This interface is implemented by mixers and presenters, and enables them to query the enhanced video renderer (EVR) for interface pointers.

## -inheritance

The <b>IMFTopologyServiceLookupClient</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTopologyServiceLookupClient</b> also has these types of members:

## -remarks

When the EVR loads the video mixer and the video presenter, the EVR queries the object for this interface and calls <a href="/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers">InitServicePointers</a>. Inside the <b>InitServicePointers</b> method, the object can query the EVR for interface pointers.

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookup">IMFTopologyServiceLookup</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
