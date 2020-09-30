---
UID: NF:wsddisco.IWSDiscoveryProvider.SetAddressFamily
title: IWSDiscoveryProvider::SetAddressFamily (wsddisco.h)
description: Specifies the IP address family (IPv4, IPv6, or both) to search when discovering WSD devices.
helpviewer_keywords: ["IWSDiscoveryProvider interface","SetAddressFamily method","IWSDiscoveryProvider.SetAddressFamily","IWSDiscoveryProvider::SetAddressFamily","SetAddressFamily","SetAddressFamily method","SetAddressFamily method","IWSDiscoveryProvider interface","WSDAPI_ADDRESSFAMILY_IPV4","WSDAPI_ADDRESSFAMILY_IPV4 | WSDAPI_ADDRESSFAMILY_IPV6","WSDAPI_ADDRESSFAMILY_IPV6","ncd.iwsdiscoveryprovider_setaddressfamily","wsddisco/IWSDiscoveryProvider::SetAddressFamily"]
old-location: ncd\iwsdiscoveryprovider_setaddressfamily.htm
tech.root: ncd
ms.assetid: 33b13cd5-ea60-4928-a220-db563c00a43c
ms.date: 12/05/2018
ms.keywords: IWSDiscoveryProvider interface,SetAddressFamily method, IWSDiscoveryProvider.SetAddressFamily, IWSDiscoveryProvider::SetAddressFamily, SetAddressFamily, SetAddressFamily method, SetAddressFamily method,IWSDiscoveryProvider interface, WSDAPI_ADDRESSFAMILY_IPV4, WSDAPI_ADDRESSFAMILY_IPV4 | WSDAPI_ADDRESSFAMILY_IPV6, WSDAPI_ADDRESSFAMILY_IPV6, ncd.iwsdiscoveryprovider_setaddressfamily, wsddisco/IWSDiscoveryProvider::SetAddressFamily
req.header: wsddisco.h
req.include-header: 
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
 - IWSDiscoveryProvider::SetAddressFamily
 - wsddisco/IWSDiscoveryProvider::SetAddressFamily
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
 - IWSDiscoveryProvider.SetAddressFamily
---

# IWSDiscoveryProvider::SetAddressFamily


## -description

Specifies the IP address family (IPv4, IPv6, or both) to search when discovering WSD devices.

## -parameters

### -param dwAddressFamily [in]

The address family to search when discovering devices.

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
Search over IPv4 addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_ADDRESSFAMILY_IPV6"></a><a id="wsdapi_addressfamily_ipv6"></a><dl>
<dt><b>WSDAPI_ADDRESSFAMILY_IPV6</b></dt>
</dl>
</td>
<td width="60%">
Search over IPv6 addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="WSDAPI_ADDRESSFAMILY_IPV4___WSDAPI_ADDRESSFAMILY_IPV6"></a><a id="wsdapi_addressfamily_ipv4___wsdapi_addressfamily_ipv6"></a><dl>
<dt><b>WSDAPI_ADDRESSFAMILY_IPV4 | WSDAPI_ADDRESSFAMILY_IPV6</b></dt>
</dl>
</td>
<td width="60%">
Search over IPv4 and IPv6 addresses.

</td>
</tr>
</table>

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

This method can be called only once on a provider. This method must be called before a notification sink is attached to the provider. That means <b>SetAddressFamily</b> must be called before <a href="/windows/desktop/api/wsddisco/nf-wsddisco-iwsdiscoveryprovider-attach">Attach</a> is called on a provider.

## -see-also

<a href="/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveryprovider">IWSDiscoveryProvider</a>