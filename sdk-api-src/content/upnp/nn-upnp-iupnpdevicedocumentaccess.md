---
UID: NN:upnp.IUPnPDeviceDocumentAccess
title: IUPnPDeviceDocumentAccess (upnp.h)
description: The IUPnPDeviceDocumentAccess interface enables an application to obtain the URL of the device description document.helpviewer_keywords: ["IUPnPDeviceDocumentAccess","IUPnPDeviceDocumentAccess interface [UPnP APIs]","IUPnPDeviceDocumentAccess interface [UPnP APIs]","described","_upnp_iupnpdevicedocumentaccess","upnp.iupnpdevicedocumentaccess","upnp/IUPnPDeviceDocumentAccess"]
old-location: upnp\iupnpdevicedocumentaccess.htm
tech.root: upnp
ms.assetid: 6d71425e-3e33-44e0-845a-4bcd05939d24
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceDocumentAccess, IUPnPDeviceDocumentAccess interface [UPnP APIs], IUPnPDeviceDocumentAccess interface [UPnP APIs],described, _upnp_iupnpdevicedocumentaccess, upnp.iupnpdevicedocumentaccess, upnp/IUPnPDeviceDocumentAccess
f1_keywords:
- upnp/IUPnPDeviceDocumentAccess
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
- IUPnPDeviceDocumentAccess
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDeviceDocumentAccess interface


## -description


The 
<b>IUPnPDeviceDocumentAccess</b> interface enables an application to obtain the URL of the device description document.
<div class="alert"><b>Note</b>  This interface does not support scripting.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceDocumentAccess</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPDeviceDocumentAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDeviceDocumentAccess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevicedocumentaccess-getdocumenturl">GetDocumentURL</a>
</td>
<td align="left" width="63%">
Returns the URL from which the device description document can be loaded.

</td>
</tr>
</table> 

