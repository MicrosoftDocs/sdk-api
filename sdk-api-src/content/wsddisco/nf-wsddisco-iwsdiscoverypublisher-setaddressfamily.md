---
UID: NF:wsddisco.IWSDiscoveryPublisher.SetAddressFamily
title: IWSDiscoveryPublisher::SetAddressFamily (wsddisco.h)
description: Specifies the IP address family (IPv4, IPv6, or both) over which the host will be published.
helpviewer_keywords: ["IWSDiscoveryPublisher interface","SetAddressFamily method","IWSDiscoveryPublisher.SetAddressFamily","IWSDiscoveryPublisher::SetAddressFamily","SetAddressFamily","SetAddressFamily method","SetAddressFamily method","IWSDiscoveryPublisher interface","WSDAPI_ADDRESSFAMILY_IPV4","WSDAPI_ADDRESSFAMILY_IPV4 | WSDAPI_ADDRESSFAMILY_IPV6","WSDAPI_ADDRESSFAMILY_IPV6","ncd.iwsdiscoverypublisher_setaddressfamily","wsddisco/IWSDiscoveryPublisher::SetAddressFamily"]
old-location: ncd\iwsdiscoverypublisher_setaddressfamily.htm
tech.root: ncd
ms.assetid: 01d16205-ca4c-44bb-865c-7fc9fb1db2e1
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryPublisher interface,SetAddressFamily method, IWSDiscoveryPublisher.SetAddressFamily, IWSDiscoveryPublisher::SetAddressFamily, SetAddressFamily, SetAddressFamily method, SetAddressFamily method,IWSDiscoveryPublisher interface, WSDAPI_ADDRESSFAMILY_IPV4, WSDAPI_ADDRESSFAMILY_IPV4 | WSDAPI_ADDRESSFAMILY_IPV6, WSDAPI_ADDRESSFAMILY_IPV6, ncd.iwsdiscoverypublisher_setaddressfamily, wsddisco/IWSDiscoveryPublisher::SetAddressFamily
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
 - IWSDiscoveryPublisher::SetAddressFamily
 - wsddisco/IWSDiscoveryPublisher::SetAddressFamily
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDiscoveryPublisher.SetAddressFamily
---

# IWSDiscoveryPublisher::SetAddressFamily


## -description

Specifies the IP address family (IPv4, IPv6, or both) over which the host will be published.

## -parameters

### -param dwAddressFamily [in]

The address family over which the host will be published.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_ADDRESSFAMILY_IPV4"></a><a id="wsdapi_addressfamily_ipv4"></a><dl>
<dt><b>WSDAPI_ADDRESSFAMILY_IPV4</b></dt>
</dl>
</td>
<td width="60%">
Publish the host over IPv4 addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_ADDRESSFAMILY_IPV6"></a><a id="wsdapi_addressfamily_ipv6"></a><dl>
<dt><b>WSDAPI_ADDRESSFAMILY_IPV6</b></dt>
</dl>
</td>
<td width="60%">
Publish the host over IPv6 addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_ADDRESSFAMILY_IPV4___WSDAPI_ADDRESSFAMILY_IPV6"></a><a id="wsdapi_addressfamily_ipv4___wsdapi_addressfamily_ipv6"></a><dl>
<dt><b>WSDAPI_ADDRESSFAMILY_IPV4 | WSDAPI_ADDRESSFAMILY_IPV6</b></dt>
</dl>
</td>
<td width="60%">
Publish the host over IPv4 and IPv6 addresses.

</td>
</tr>
</table>

## -returns

Possible return values include, but are not limited to, the following:

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwAddressFamily</i> has a value other than WSDAPI_ADDRESSFAMILY_IPV4, WSDAPI_ADDRESSFAMILY_IPV6, or WSDAPI_ADDRESSFAMILY_IPV4 | WSDAPI_ADDRESSFAMILY_IPV6.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDFUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The address family has already been set for this publisher.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(WSAESOCKTNOSUPPORT)</b></dt>
</dl>
</td>
<td width="60%">
The system does not support the address family specified by <i>dwAddressFamily</i>.

</td>
</tr>
</table>

## -remarks

This method must be called before a notification sink is attached to the publisher.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoverypublisher">IWSDiscoveryPublisher</a>