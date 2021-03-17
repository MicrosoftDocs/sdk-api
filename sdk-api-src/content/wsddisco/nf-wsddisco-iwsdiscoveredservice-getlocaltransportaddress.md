---
UID: NF:wsddisco.IWSDiscoveredService.GetLocalTransportAddress
title: IWSDiscoveredService::GetLocalTransportAddress (wsddisco.h)
description: Retrieves the string representation of the local transport (IP) address.
helpviewer_keywords: ["GetLocalTransportAddress","GetLocalTransportAddress method","GetLocalTransportAddress method","IWSDiscoveredService interface","IWSDiscoveredService interface","GetLocalTransportAddress method","IWSDiscoveredService.GetLocalTransportAddress","IWSDiscoveredService::GetLocalTransportAddress","ncd.iwsdiscoveredservice_getlocaltransportaddress","wsddisco/IWSDiscoveredService::GetLocalTransportAddress"]
old-location: ncd\iwsdiscoveredservice_getlocaltransportaddress.htm
tech.root: ncd
ms.assetid: a7127ce7-175f-463e-8d54-0c637639a108
ms.date: 12/05/2018
ms.keywords: GetLocalTransportAddress, GetLocalTransportAddress method, GetLocalTransportAddress method,IWSDiscoveredService interface, IWSDiscoveredService interface,GetLocalTransportAddress method, IWSDiscoveredService.GetLocalTransportAddress, IWSDiscoveredService::GetLocalTransportAddress, ncd.iwsdiscoveredservice_getlocaltransportaddress, wsddisco/IWSDiscoveredService::GetLocalTransportAddress
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
 - IWSDiscoveredService::GetLocalTransportAddress
 - wsddisco/IWSDiscoveredService::GetLocalTransportAddress
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
 - IWSDiscoveredService.GetLocalTransportAddress
---

# IWSDiscoveredService::GetLocalTransportAddress


## -description

Retrieves the string representation of the local transport (IP) address.

## -parameters

### -param ppszLocalTransportAddress [out]

String representation of the local transport (IP) address. Is <b>NULL</b> if not available.
Do not deallocate the output string.

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
<i>ppszLocalTransportAddress</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The resulting pointer value is only valid for the lifetime of the <a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a> object.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a>