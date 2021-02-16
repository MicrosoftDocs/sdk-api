---
UID: NF:upnp.IUPnPAddressFamilyControl.GetAddressFamily
title: IUPnPAddressFamilyControl::GetAddressFamily (upnp.h)
description: The GetAddressFamily method retrieves the current value of the address family flag of the Device Finder object.
helpviewer_keywords: ["GetAddressFamily","GetAddressFamily method [UPnP APIs]","GetAddressFamily method [UPnP APIs]","IUPnPAddressFamilyControl interface","IUPnPAddressFamilyControl interface [UPnP APIs]","GetAddressFamily method","IUPnPAddressFamilyControl.GetAddressFamily","IUPnPAddressFamilyControl::GetAddressFamily","UPNP_ADDRESSFAMILY_BOTH","UPNP_ADDRESSFAMILY_IPv4","UPNP_ADDRESSFAMILY_IPv6","upnp.iupnpaddressfamilycontrol_getaddressfamily","upnp/IUPnPAddressFamilyControl::GetAddressFamily"]
old-location: upnp\iupnpaddressfamilycontrol_getaddressfamily.htm
tech.root: upnp
ms.assetid: 3ad0897e-e128-4b49-92c1-eaf2ac516c3b
ms.date: 12/05/2018
ms.keywords: GetAddressFamily, GetAddressFamily method [UPnP APIs], GetAddressFamily method [UPnP APIs],IUPnPAddressFamilyControl interface, IUPnPAddressFamilyControl interface [UPnP APIs],GetAddressFamily method, IUPnPAddressFamilyControl.GetAddressFamily, IUPnPAddressFamilyControl::GetAddressFamily, UPNP_ADDRESSFAMILY_BOTH, UPNP_ADDRESSFAMILY_IPv4, UPNP_ADDRESSFAMILY_IPv6, upnp.iupnpaddressfamilycontrol_getaddressfamily, upnp/IUPnPAddressFamilyControl::GetAddressFamily
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IUPnPAddressFamilyControl::GetAddressFamily
 - upnp/IUPnPAddressFamilyControl::GetAddressFamily
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
 - IUPnPAddressFamilyControl.GetAddressFamily
---

# IUPnPAddressFamilyControl::GetAddressFamily


## -description

The <b>GetAddressFamily</b> method retrieves the current value of the address family flag of the Device Finder object.

## -parameters

### -param pdwFlags [out, retval]

Pointer to an integer (4-byte value) that indicates the address family.

The following values are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UPNP_ADDRESSFAMILY_IPv4"></a><a id="upnp_addressfamily_ipv4"></a><a id="UPNP_ADDRESSFAMILY_IPV4"></a><dl>
<dt><b>UPNP_ADDRESSFAMILY_IPv4</b></dt>
</dl>
</td>
<td width="60%">
IPv4 (IP version 4)

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_ADDRESSFAMILY_IPv6"></a><a id="upnp_addressfamily_ipv6"></a><a id="UPNP_ADDRESSFAMILY_IPV6"></a><dl>
<dt><b>UPNP_ADDRESSFAMILY_IPv6</b></dt>
</dl>
</td>
<td width="60%">
IPv6 (IP version 6)

</td>
</tr>
<tr>
<td width="40%"><a id="UPNP_ADDRESSFAMILY_BOTH"></a><a id="upnp_addressfamily_both"></a><dl>
<dt><b>UPNP_ADDRESSFAMILY_BOTH</b></dt>
</dl>
</td>
<td width="60%">
IPv4 and IPv6

</td>
</tr>
</table>

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpaddressfamilycontrol">IUPnPAddressFamilyControl</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpaddressfamilycontrol-setaddressfamily">SetAddressFamily</a>