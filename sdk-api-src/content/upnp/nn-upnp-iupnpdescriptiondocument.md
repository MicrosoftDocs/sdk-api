---
UID: NN:upnp.IUPnPDescriptionDocument
title: IUPnPDescriptionDocument (upnp.h)
description: The IUPnPDescriptionDocument interface enables an application to load a device description.
helpviewer_keywords: ["IUPnPDescriptionDocument","IUPnPDescriptionDocument interface [UPnP APIs]","IUPnPDescriptionDocument interface [UPnP APIs]","described","_upnp_iupnpdescriptiondocument","upnp.iupnpdescriptiondocument","upnp/IUPnPDescriptionDocument"]
old-location: upnp\iupnpdescriptiondocument.htm
tech.root: upnp
ms.assetid: 25bd3abd-b270-4609-93bb-a786ccaa95dd
ms.date: 12/05/2018
ms.keywords: IUPnPDescriptionDocument, IUPnPDescriptionDocument interface [UPnP APIs], IUPnPDescriptionDocument interface [UPnP APIs],described, _upnp_iupnpdescriptiondocument, upnp.iupnpdescriptiondocument, upnp/IUPnPDescriptionDocument
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
 - IUPnPDescriptionDocument
 - upnp/IUPnPDescriptionDocument
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
 - IUPnPDescriptionDocument
---

# IUPnPDescriptionDocument interface


## -description

The 
<b>IUPnPDescriptionDocument</b> interface enables an application to load a device description.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDescriptionDocument</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUPnPDescriptionDocument</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUPnPDescriptionDocument</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-abort">Abort</a>
</td>
<td align="left" width="63%">
Stops an asynchronous load operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-devicebyudn">DeviceByUDN</a>
</td>
<td align="left" width="63%">
Returns a device from the currently loaded document with the specified unique device name (UDN).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-load">Load</a>
</td>
<td align="left" width="63%">
Loads a document synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">LoadAsync</a>
</td>
<td align="left" width="63%">
Loads a document asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-rootdevice">RootDevice</a>
</td>
<td align="left" width="63%">
Returns the root device of the loaded document's device tree.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDescriptionDocument</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-get_loadresult">LoadResult</a>


</td>
<td align="left" width="63%">
Result code that indicates the success or failure of a completed load operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-get_readystate">ReadyState</a>


</td>
<td align="left" width="63%">
Status of the document load operation.

</td>
</tr>
</table>

