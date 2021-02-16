---
UID: NF:wsddisco.IWSDiscoveredService.GetEndpointReference
title: IWSDiscoveredService::GetEndpointReference (wsddisco.h)
description: Retrieves a WS-Addressing address referencing an endpoint of the remote device.
helpviewer_keywords: ["GetEndpointReference","GetEndpointReference method","GetEndpointReference method","IWSDiscoveredService interface","IWSDiscoveredService interface","GetEndpointReference method","IWSDiscoveredService.GetEndpointReference","IWSDiscoveredService::GetEndpointReference","ncd.iwsdiscoveredservice_getendpointreference","wsddisco/IWSDiscoveredService::GetEndpointReference"]
old-location: ncd\iwsdiscoveredservice_getendpointreference.htm
tech.root: ncd
ms.assetid: 656ff77d-765e-4c30-8e5d-560d121dc368
ms.date: 12/05/2018
ms.keywords: GetEndpointReference, GetEndpointReference method, GetEndpointReference method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetEndpointReference method, IWSDiscoveredService.GetEndpointReference, IWSDiscoveredService::GetEndpointReference, ncd.iwsdiscoveredservice_getendpointreference, wsddisco/IWSDiscoveredService::GetEndpointReference
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDiscoveredService::GetEndpointReference
 - wsddisco/IWSDiscoveredService::GetEndpointReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveredService.GetEndpointReference
---

# IWSDiscoveredService::GetEndpointReference


## -description

Retrieves a WS-Addressing address referencing an endpoint of the remote device.

## -parameters

### -param ppEndpointReference [out]

A WS-Addressing address referencing an endpoint of the remote device. For details, see <a href="/windows/desktop/api/wsdtypes/ns-wsdtypes-wsd_endpoint_reference">WSD_ENDPOINT_REFERENCE</a>. Do not deallocate the output structure.

## -returns

This method can return one of these values.


Possible return values include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppEndPointReference</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The resulting pointer value is only valid for the lifetime of the <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a> object.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a>