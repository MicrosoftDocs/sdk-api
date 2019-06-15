---
UID: NN:evr.IMFTopologyServiceLookup
title: IMFTopologyServiceLookup (evr.h)
author: windows-sdk-content
description: Enables a custom video mixer or video presenter to get interface pointers from the Enhanced Video Renderer (EVR).
old-location: mf\imftopologyservicelookup.htm
tech.root: medfound
ms.assetid: a912c17a-40ef-441c-bfc9-7ef49d22070f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFTopologyServiceLookup, IMFTopologyServiceLookup interface [Media Foundation], IMFTopologyServiceLookup interface [Media Foundation],described, a912c17a-40ef-441c-bfc9-7ef49d22070f, evr/IMFTopologyServiceLookup, mf.imftopologyservicelookup
ms.topic: interface
f1_keywords: ["evr/IMFTopologyServiceLookup"]
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFTopologyServiceLookup interface


## -description


Enables a custom video mixer or video presenter to get interface pointers from the <a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR). The mixer can also use this interface to get interface pointers from the presenter, and the presenter can use it to get interface pointers from the mixer.

To use this interface, implement the <a href="https://docs.microsoft.com/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient">IMFTopologyServiceLookupClient</a> interface on your custom mixer or presenter. The EVR calls <a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers">IMFTopologyServiceLookupClient::InitServicePointers</a> with a pointer to the EVR's <b>IMFTopologyServiceLookup</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFTopologyServiceLookup</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFTopologyServiceLookup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFTopologyServiceLookup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice">LookupService</a>
</td>
<td align="left" width="63%">
Retrieves an interface from the EVR, or from the video mixer or video presenter.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

