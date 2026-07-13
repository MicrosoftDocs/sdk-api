---
UID: NF:upnp.IUPnPDescriptionDocument.Abort
title: IUPnPDescriptionDocument::Abort (upnp.h)
description: The Abort method stops an asynchronous load operation started by IUPnPDescriptionDocument::LoadAsync.
helpviewer_keywords: ["Abort","Abort method [UPnP APIs]","Abort method [UPnP APIs]","IUPnPDescriptionDocument interface","IUPnPDescriptionDocument interface [UPnP APIs]","Abort method","IUPnPDescriptionDocument.Abort","IUPnPDescriptionDocument::Abort","_upnp_iupnpdescriptiondocument_abort","upnp.iupnpdescriptiondocument_abort","upnp/IUPnPDescriptionDocument::Abort"]
old-location: upnp\iupnpdescriptiondocument_abort.htm
tech.root: upnp
ms.assetid: 26f5a7f0-7d29-47a6-9f43-6b0d921342ae
ms.date: 12/05/2018
ms.keywords: Abort, Abort method [UPnP APIs], Abort method [UPnP APIs],IUPnPDescriptionDocument interface, IUPnPDescriptionDocument interface [UPnP APIs],Abort method, IUPnPDescriptionDocument.Abort, IUPnPDescriptionDocument::Abort, _upnp_iupnpdescriptiondocument_abort, upnp.iupnpdescriptiondocument_abort, upnp/IUPnPDescriptionDocument::Abort
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPDescriptionDocument::Abort
 - upnp/IUPnPDescriptionDocument::Abort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDescriptionDocument.Abort
---

# IUPnPDescriptionDocument::Abort


## -description

The 
<b>Abort</b> method stops an asynchronous load operation started by 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">IUPnPDescriptionDocument::LoadAsync</a>.



## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocument">IUPnPDescriptionDocument</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">IUPnPDescriptionDocument::LoadAsync</a>
