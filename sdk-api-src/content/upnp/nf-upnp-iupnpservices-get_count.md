---
UID: NF:upnp.IUPnPServices.get_Count
title: IUPnPServices::get_Count (upnp.h)
description: The Count property specifies the number of services in the collection.
helpviewer_keywords: ["IUPnPServices interface [UPnP APIs]","get_Count method","IUPnPServices.get_Count","IUPnPServices::get_Count","_upnp_iupnpservices_count","get_Count","get_Count method [UPnP APIs]","get_Count method [UPnP APIs]","IUPnPServices interface","upnp.iupnpservices_count","upnp/IUPnPServices::get_Count"]
old-location: upnp\iupnpservices_count.htm
tech.root: upnp
ms.assetid: 33d90664-825a-4562-82ae-249b329743ac
ms.date: 12/05/2018
ms.keywords: IUPnPServices interface [UPnP APIs],get_Count method, IUPnPServices.get_Count, IUPnPServices::get_Count, _upnp_iupnpservices_count, get_Count, get_Count method [UPnP APIs], get_Count method [UPnP APIs],IUPnPServices interface, upnp.iupnpservices_count, upnp/IUPnPServices::get_Count
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
 - IUPnPServices::get_Count
 - upnp/IUPnPServices::get_Count
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
 - IUPnPServices.get_Count
---

# IUPnPServices::get_Count


## -description

The 
<b>Count</b> property specifies the number of services in the collection.

## -parameters

### -param plCount [out]

Receives a reference to the number of services in the collection.

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