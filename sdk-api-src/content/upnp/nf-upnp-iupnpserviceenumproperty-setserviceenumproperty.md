---
UID: NF:upnp.IUPnPServiceEnumProperty.SetServiceEnumProperty
title: IUPnPServiceEnumProperty::SetServiceEnumProperty (upnp.h)
description: The SetServiceEnumProperty method is used to indicate opt-in to the delayed Service Control Protocol Description (SCPD) download and event subscription for the IUPnPService objects enumerated from the IUPnPServices object.
helpviewer_keywords: ["IUPnPServiceEnumProperty interface [UPnP APIs]","SetServiceEnumProperty method","IUPnPServiceEnumProperty.SetServiceEnumProperty","IUPnPServiceEnumProperty::SetServiceEnumProperty","SetServiceEnumProperty","SetServiceEnumProperty method [UPnP APIs]","SetServiceEnumProperty method [UPnP APIs]","IUPnPServiceEnumProperty interface","upnp.iupnpserviceenumproperty_setserviceenumproperty","upnp/IUPnPServiceEnumProperty::SetServiceEnumProperty"]
old-location: upnp\iupnpserviceenumproperty_setserviceenumproperty.htm
tech.root: upnp
ms.assetid: B138A230-7523-4803-ACE8-4F636DD54D86
ms.date: 12/05/2018
ms.keywords: IUPnPServiceEnumProperty interface [UPnP APIs],SetServiceEnumProperty method, IUPnPServiceEnumProperty.SetServiceEnumProperty, IUPnPServiceEnumProperty::SetServiceEnumProperty, SetServiceEnumProperty, SetServiceEnumProperty method [UPnP APIs], SetServiceEnumProperty method [UPnP APIs],IUPnPServiceEnumProperty interface, upnp.iupnpserviceenumproperty_setserviceenumproperty, upnp/IUPnPServiceEnumProperty::SetServiceEnumProperty
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUPnPServiceEnumProperty::SetServiceEnumProperty
 - upnp/IUPnPServiceEnumProperty::SetServiceEnumProperty
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
 - IUPnPServiceEnumProperty.SetServiceEnumProperty
---

# IUPnPServiceEnumProperty::SetServiceEnumProperty


## -description

The <b>SetServiceEnumProperty</b> method is used to indicate opt-in to the delayed Service Control Protocol Description (SCPD) download and event subscription for the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a> objects enumerated from the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpservices">IUPnPServices</a> object.

## -parameters

### -param dwMask

Specifies a bit-wise flag to indicate an opt-in to the delayed SCPD download and even subscription. Possible values include:

<table>
<tr>
<th>Flag</th>
<th>Value</th>
</tr>
<tr>
<td>UPNP_SERVICE_DELAY_SCPD_AND_SUBSCRIPTION</td>
<td>0x1</td>
</tr>
</table>

## -returns

Returns <b>S_OK</b> on success. Otherwise, this method returns <b>E_FAIL</b>.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceenumproperty">IUPnPServiceEnumProperty</a>