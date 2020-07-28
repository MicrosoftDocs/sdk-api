---
UID: NN:strmif.IAMFilterGraphCallback
title: IAMFilterGraphCallback (strmif.h)
description: The IAMFilterGraphCallback interface provides a callback mechanism during graph building.To use this interface, implement the interface in your application or client object.
helpviewer_keywords: ["IAMFilterGraphCallback","IAMFilterGraphCallback interface [DirectShow]","IAMFilterGraphCallback interface [DirectShow]","described","IAMFilterGraphCallbackInterface","dshow.iamfiltergraphcallback","strmif/IAMFilterGraphCallback"]
old-location: dshow\iamfiltergraphcallback.htm
tech.root: dshow
ms.assetid: 064acc6a-ba2f-4394-a3bf-a9b70e30e07e
ms.date: 12/05/2018
ms.keywords: IAMFilterGraphCallback, IAMFilterGraphCallback interface [DirectShow], IAMFilterGraphCallback interface [DirectShow],described, IAMFilterGraphCallbackInterface, dshow.iamfiltergraphcallback, strmif/IAMFilterGraphCallback
f1_keywords:
- strmif/IAMFilterGraphCallback
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IAMFilterGraphCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMFilterGraphCallback interface


## -description



The <code>IAMFilterGraphCallback</code> interface provides a callback mechanism during graph building.

To use this interface, implement the interface in your application or client object. Query the Filter Graph Manager for the <b>IObjectWithSite</b> interface and call the <b>IObjectWithSite::SetSite</b> method with a pointer to your implementation of the interface. During graph building, if the Filter Graph Manager fails to render a pin, it calls the <b>UnabletoRender</b> method. The client can then take appropriate action, such as providing an error message for the user or registering a new filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMFilterGraphCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMFilterGraphCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMFilterGraphCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iamfiltergraphcallback-unabletorender">UnableToRender</a>
</td>
<td align="left" width="63%">
Informs the client that no combination of filters could be found to render the specified pin.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamgraphbuildercallback">IAMGraphBuilderCallback Interface</a>
 

 

