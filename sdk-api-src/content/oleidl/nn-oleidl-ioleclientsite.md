---
UID: NN:oleidl.IOleClientSite
title: IOleClientSite (oleidl.h)
description: Provides the primary means by which an embedded object obtains information about the location and extent of its display site, its moniker, its user interface, and other resources provided by its container.
helpviewer_keywords: ["IOleClientSite","IOleClientSite interface [COM]","IOleClientSite interface [COM]","described","_ole_ioleclientsite","com.ioleclientsite","oleidl/IOleClientSite"]
old-location: com\ioleclientsite.htm
tech.root: com
ms.assetid: dafee149-926a-4d08-a43d-5847682db645
ms.date: 12/05/2018
ms.keywords: IOleClientSite, IOleClientSite interface [COM], IOleClientSite interface [COM],described, _ole_ioleclientsite, com.ioleclientsite, oleidl/IOleClientSite
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleClientSite
 - oleidl/IOleClientSite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleClientSite
---

# IOleClientSite interface


## -description

Provides the primary means by which an embedded object obtains information about the location and extent of its display site, its moniker, its user interface, and other resources provided by its container. An object server calls <b>IOleClientSite</b> to request services from the container. A container must provide one instance of <b>IOleClientSite</b> for every compound-document object it contains.
<div class="alert"><b>Note</b>  This interface is not supported for use across machine boundaries.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleClientSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleClientSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleClientSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getcontainer">GetContainer</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the object's container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-getmoniker">GetMoniker</a>
</td>
<td align="left" width="63%">
Retrieves a moniker for the object's client site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-onshowwindow">OnShowWindow</a>
</td>
<td align="left" width="63%">
Notifies a container when an embedded object's window is about to become visible or invisible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-requestnewobjectlayout">RequestNewObjectLayout</a>
</td>
<td align="left" width="63%">
Asks a container to resize the display site for embedded objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-saveobject">SaveObject</a>
</td>
<td align="left" width="63%">
Saves the embedded object associated with the client site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleclientsite-showobject">ShowObject</a>
</td>
<td align="left" width="63%">
Asks a container to display its object to the user.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a>



<a href="/windows/desktop/api/docobj/nn-docobj-ioledocumentsite">IOleDocumentSite</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplacesite">IOleInPlaceSite</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getclientsite">IOleObject::GetClientSite</a>