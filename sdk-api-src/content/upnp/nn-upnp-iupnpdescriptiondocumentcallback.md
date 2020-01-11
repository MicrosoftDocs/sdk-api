---
UID: NN:upnp.IUPnPDescriptionDocumentCallback
title: IUPnPDescriptionDocumentCallback (upnp.h)
description: The IUPnPDescriptionDocumentCallback interface allows the UPnP framework to communicate the results of an asynchronous load operation to an application.
old-location: upnp\iupnpdescriptiondocumentcallback.htm
tech.root: upnp
ms.assetid: 0c9071d8-2ec1-49fe-976d-0c63f9de8b61
ms.date: 12/05/2018
ms.keywords: IUPnPDescriptionDocumentCallback, IUPnPDescriptionDocumentCallback interface [UPnP APIs], IUPnPDescriptionDocumentCallback interface [UPnP APIs],described, _upnp_iupnpdescriptiondocumentcallback, upnp.iupnpdescriptiondocumentcallback, upnp/IUPnPDescriptionDocumentCallback
f1_keywords:
- upnp/IUPnPDescriptionDocumentCallback
dev_langs:
- c++
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Upnp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Upnp.dll
api_name:
- IUPnPDescriptionDocumentCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDescriptionDocumentCallback interface


## -description


The 
<b>IUPnPDescriptionDocumentCallback</b> interface allows the UPnP framework to communicate the results of an asynchronous load operation to an application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDescriptionDocumentCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPDescriptionDocumentCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDescriptionDocumentCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocumentcallback-loadcomplete">LoadComplete</a>
</td>
<td align="left" width="63%">
Invoked by the UPnP framework to notify the application that a load operation has been completed.

</td>
</tr>
</table> 

