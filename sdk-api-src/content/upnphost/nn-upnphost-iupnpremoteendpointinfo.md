---
UID: NN:upnphost.IUPnPRemoteEndpointInfo
title: IUPnPRemoteEndpointInfo (upnphost.h)
author: windows-sdk-content
description: The IUPnPRemoteEndpointInfo interface allows a hosted device to obtain information about a requester (that is, a control point) and the request.
old-location: upnp\iupnpremoteendpointinfo.htm
tech.root: upnp
ms.assetid: 32e246cd-50eb-4221-8166-a7cd8ed42d69
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPRemoteEndpointInfo, IUPnPRemoteEndpointInfo interface [UPnP APIs], IUPnPRemoteEndpointInfo interface [UPnP APIs],described, upnp.iupnpremoteendpointinfo, upnphost/IUPnPRemoteEndpointInfo
ms.topic: interface
f1_keywords: 
 - "upnphost/IUPnPRemoteEndpointInfo"
dev_langs:
 - c++
req.header: upnphost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
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
req.dll: Upnphost.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPRemoteEndpointInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPRemoteEndpointInfo interface


## -description


The <b>IUPnPRemoteEndpointInfo</b> interface allows a hosted device to obtain information about a requester (that is,  a control point) and the request.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPRemoteEndpointInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPRemoteEndpointInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPRemoteEndpointInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpremoteendpointinfo-getdwordvalue">GetDwordValue</a>
</td>
<td align="left" width="63%">
Gets a 4-byte value that provides information about either a request or requester.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpremoteendpointinfo-getguidvalue">GetGuidValue</a>
</td>
<td align="left" width="63%">
Currently not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpremoteendpointinfo-getstringvalue">GetStringValue</a>
</td>
<td align="left" width="63%">
Gets a string that provides information about either a request or requester.

</td>
</tr>
</table> 

