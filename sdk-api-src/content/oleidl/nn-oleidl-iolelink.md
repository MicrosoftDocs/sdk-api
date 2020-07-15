---
UID: NN:oleidl.IOleLink
title: IOleLink (oleidl.h)
description: Enables a linked object to provide its container with functions pertaining to linking.
helpviewer_keywords: ["IOleLink","IOleLink interface [COM]","IOleLink interface [COM]","described","_ole_iolelink","com.iolelink","oleidl/IOleLink"]
old-location: com\iolelink.htm
tech.root: com
ms.assetid: 4a34a90d-df1b-4bbf-8365-9d741c18ff74
ms.date: 12/05/2018
ms.keywords: IOleLink, IOleLink interface [COM], IOleLink interface [COM],described, _ole_iolelink, com.iolelink, oleidl/IOleLink
f1_keywords:
- oleidl/IOleLink
dev_langs:
- c++
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- OleIdl.h
api_name:
- IOleLink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleLink interface


## -description


Enables a linked object to provide its container with functions pertaining to linking. The most important of these functions is binding to the link source, that is, activating the connection to the document that stores the linked object's native data. <b>IOleLink</b> also defines functions for managing information about the linked object, such as the location of the link source and the cached presentation data for the linked object.

A container application can distinguish between embedded objects and linked objects by querying for <b>IOleLink</b>; only linked objects implement <b>IOleLink</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleLink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOleLink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleLink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindifrunning">BindIfRunning</a>
</td>
<td align="left" width="63%">
Activates the connection between the linked object and the link source if the link source is already running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource">BindToSource</a>
</td>
<td align="left" width="63%">
Activates the connection to the link source by binding the moniker stored within the linked object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-getboundsource">GetBoundSource</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the link source if the connection is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcedisplayname">GetSourceDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the link source of the linked object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-getsourcemoniker">GetSourceMoniker</a>
</td>
<td align="left" width="63%">
Retrieves the moniker identifying the link source of a linked object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-getupdateoptions">GetUpdateOptions</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating how often the linked object updates its cached data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-setsourcedisplayname">SetSourceDisplayName</a>
</td>
<td align="left" width="63%">
Sets the display name for the link source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-setsourcemoniker">SetSourceMoniker</a>
</td>
<td align="left" width="63%">
Sets the moniker for the link source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-setupdateoptions">SetUpdateOptions</a>
</td>
<td align="left" width="63%">
Specifies how often a linked object should update its cached data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-unbindsource">UnbindSource</a>
</td>
<td align="left" width="63%">
Breaks the connection between a linked object and its link source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-iolelink-update">Update</a>
</td>
<td align="left" width="63%">
Updates the compound document's cached data for a linked object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkcontainera">IOleUILinkContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oledlg/nf-oledlg-oleuieditlinksa">OleUIEditLinks</a>
 

 

