---
UID: NN:upnp.IUPnPDeviceDocumentAccessEx
title: IUPnPDeviceDocumentAccessEx (upnp.h)
description: Provides a method to obtain the entire XML device description document for a specific device.
helpviewer_keywords: ["IUPnPDeviceDocumentAccessEx","IUPnPDeviceDocumentAccessEx interface [UPnP APIs]","IUPnPDeviceDocumentAccessEx interface [UPnP APIs]","described","upnp.iupnpdevicedocumentaccessex","upnp/IUPnPDeviceDocumentAccessEx"]
old-location: upnp\iupnpdevicedocumentaccessex.htm
tech.root: upnp
ms.assetid: 9ea79bbb-3841-4704-9606-56fcd2f8bf89
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceDocumentAccessEx, IUPnPDeviceDocumentAccessEx interface [UPnP APIs], IUPnPDeviceDocumentAccessEx interface [UPnP APIs],described, upnp.iupnpdevicedocumentaccessex, upnp/IUPnPDeviceDocumentAccessEx
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IUPnPDeviceDocumentAccessEx
 - upnp/IUPnPDeviceDocumentAccessEx
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
 - IUPnPDeviceDocumentAccessEx
---

# IUPnPDeviceDocumentAccessEx interface


## -description

The <b>IUPnPDeviceDocumentAccessEx</b> interface provides a method to obtain the entire XML device description document for a specific device.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDeviceDocumentAccessEx</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPDeviceDocumentAccessEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPDeviceDocumentAccessEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicedocumentaccessex-getdocument">GetDocument</a>
</td>
<td align="left" width="63%">
Retrieves the XML device description document for a UPnP device.

</td>
</tr>
</table>

## -remarks

This interface is obtained by calling QueryInterface on the same object that provides an implementation of <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>, after which <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicedocumentaccessex-getdocument">GetDocument</a> can be called on it.

## -see-also

<a href="/windows/desktop/UPnP/control-point-api-with-upnp-technology-reference">Control Point API Reference</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicedocumentaccess">IUPnPDeviceDocumentAccess</a>