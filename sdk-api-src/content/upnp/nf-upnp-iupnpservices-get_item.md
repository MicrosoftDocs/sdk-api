---
UID: NF:upnp.IUPnPServices.get_Item
title: IUPnPServices::get_Item (upnp.h)
description: The Item property specifies the IUPnPService interface for a service, identified by the service ID, in the collection.
helpviewer_keywords: ["IUPnPServices interface [UPnP APIs]","get_Item method","IUPnPServices.get_Item","IUPnPServices::get_Item","_upnp_iupnpservices_item","get_Item","get_Item method [UPnP APIs]","get_Item method [UPnP APIs]","IUPnPServices interface","upnp.iupnpservices_item","upnp/IUPnPServices::get_Item"]
old-location: upnp\iupnpservices_item.htm
tech.root: upnp
ms.assetid: e59e9b9c-986d-46de-9ce7-19eaad824953
ms.date: 12/05/2018
ms.keywords: IUPnPServices interface [UPnP APIs],get_Item method, IUPnPServices.get_Item, IUPnPServices::get_Item, _upnp_iupnpservices_item, get_Item, get_Item method [UPnP APIs], get_Item method [UPnP APIs],IUPnPServices interface, upnp.iupnpservices_item, upnp/IUPnPServices::get_Item
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
 - IUPnPServices::get_Item
 - upnp/IUPnPServices::get_Item
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
 - IUPnPServices.get_Item
---

# IUPnPServices::get_Item


## -description

The 
<b>Item</b> property specifies the 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a> interface for a  service, identified by the service ID, in the collection.

## -parameters

### -param bstrServiceId [in]

Specifies a service in the collection.

### -param ppService [out]

Receives a reference to an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a> interface for the specified service.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h, or one of the following UPnP-specific return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DOCUMENT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The service description contained an error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_EVENT_SUBSCRIPTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Failed to subscribe to the event source.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservices">IUPnPServices</a>