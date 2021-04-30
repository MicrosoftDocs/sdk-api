---
UID: NS:wnvapi._WNV_PROVIDER_ADDRESS_CHANGE_PARAM
title: WNV_PROVIDER_ADDRESS_CHANGE_PARAM (wnvapi.h)
description: Specifies the provider address's DAD (duplicate address detection) status change, which causes the Windows Network Virtualization (WNV) driver to generate a WnvObjectChangeType notification that specifies the WnvProviderAddressType object type containing this structure.
helpviewer_keywords: ["*PWNV_PROVIDER_ADDRESS_CHANGE_PARAM","IpDadStateDeprecated","IpDadStateDuplicate","IpDadStateInvalid","IpDadStatePreferred","IpDadStateTentative","PWNV_PROVIDER_ADDRESS_CHANGE_PARAM","PWNV_PROVIDER_ADDRESS_CHANGE_PARAM structure pointer [Windows Network Virtualization]","WNV_PROVIDER_ADDRESS_CHANGE_PARAM","WNV_PROVIDER_ADDRESS_CHANGE_PARAM structure [Windows Network Virtualization]","wnv.wnv_provider_address_change_param","wnvapi/PWNV_PROVIDER_ADDRESS_CHANGE_PARAM","wnvapi/WNV_PROVIDER_ADDRESS_CHANGE_PARAM"]
old-location: wnv\wnv_provider_address_change_param.htm
tech.root: wnv
ms.assetid: 9FC20DFE-663C-47ED-8183-76C10D4E7615
ms.date: 12/05/2018
ms.keywords: '*PWNV_PROVIDER_ADDRESS_CHANGE_PARAM, IpDadStateDeprecated, IpDadStateDuplicate, IpDadStateInvalid, IpDadStatePreferred, IpDadStateTentative, PWNV_PROVIDER_ADDRESS_CHANGE_PARAM, PWNV_PROVIDER_ADDRESS_CHANGE_PARAM structure pointer [Windows Network Virtualization], WNV_PROVIDER_ADDRESS_CHANGE_PARAM, WNV_PROVIDER_ADDRESS_CHANGE_PARAM structure [Windows Network Virtualization], wnv.wnv_provider_address_change_param, wnvapi/PWNV_PROVIDER_ADDRESS_CHANGE_PARAM, wnvapi/WNV_PROVIDER_ADDRESS_CHANGE_PARAM'
req.header: wnvapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WNV_PROVIDER_ADDRESS_CHANGE_PARAM, *PWNV_PROVIDER_ADDRESS_CHANGE_PARAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WNV_PROVIDER_ADDRESS_CHANGE_PARAM
 - wnvapi/_WNV_PROVIDER_ADDRESS_CHANGE_PARAM
 - PWNV_PROVIDER_ADDRESS_CHANGE_PARAM
 - wnvapi/PWNV_PROVIDER_ADDRESS_CHANGE_PARAM
 - WNV_PROVIDER_ADDRESS_CHANGE_PARAM
 - wnvapi/WNV_PROVIDER_ADDRESS_CHANGE_PARAM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wnvapi.h
api_name:
 - WNV_PROVIDER_ADDRESS_CHANGE_PARAM
---

# WNV_PROVIDER_ADDRESS_CHANGE_PARAM structure


## -description

Specifies the provider address's DAD (duplicate address detection) status change, which causes the Windows Network Virtualization (WNV) driver to generate a <b>WnvObjectChangeType</b> notification that specifies the <b>WnvProviderAddressType</b> object type containing this structure.

## -struct-fields

### -field PAFamily

Type: <b>ADDRESS_FAMILY</b>

The address family (<b>AF_INET</b> or <b>AF_INET6</b>) for the provider address.

### -field PA

Type: <b><a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_ip_address">WNV_IP_ADDRESS</a></b>

The IP address object for the provider address, which is the matching IP address used on the physical network for the customer address.

### -field AddressState

Type: <b><a href="/previous-versions/windows/hardware/drivers/ff568758(v=vs.85)">NL_DAD_STATE</a></b>

A value of the <a href="/previous-versions/windows/hardware/drivers/ff568758(v=vs.85)">NL_DAD_STATE</a> enumeration that represents the new DAD state. Duplicate address detection is applicable to both IPv4 and IPv6 addresses.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IpDadStateInvalid"></a><a id="ipdadstateinvalid"></a><a id="IPDADSTATEINVALID"></a><dl>
<dt><b>IpDadStateInvalid</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The DAD state is not valid. 

</td>
</tr>
<tr>
<td width="40%"><a id="IpDadStateTentative"></a><a id="ipdadstatetentative"></a><a id="IPDADSTATETENTATIVE"></a><dl>
<dt><b>IpDadStateTentative</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The DAD state is tentative. 

</td>
</tr>
<tr>
<td width="40%"><a id="IpDadStateDuplicate"></a><a id="ipdadstateduplicate"></a><a id="IPDADSTATEDUPLICATE"></a><dl>
<dt><b>IpDadStateDuplicate</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A duplicate IP address has been detected. 

</td>
</tr>
<tr>
<td width="40%"><a id="IpDadStateDeprecated"></a><a id="ipdadstatedeprecated"></a><a id="IPDADSTATEDEPRECATED"></a><dl>
<dt><b>IpDadStateDeprecated</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The IP address has been deprecated.

</td>
</tr>
<tr>
<td width="40%"><a id="IpDadStatePreferred"></a><a id="ipdadstatepreferred"></a><a id="IPDADSTATEPREFERRED"></a><dl>
<dt><b>IpDadStatePreferred</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The IP address is the preferred address. 

</td>
</tr>
</table>

## -remarks

For a detailed description of network virtualization concepts and terminology, refer to <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj134230(v=ws.11)">Hyper-V Network Virtualization Overview</a>.

## -see-also

<a href="/windows/desktop/api/wnvapi/ne-wnvapi-wnv_notification_type">WNV_NOTIFICATION_TYPE</a>



<a href="/windows/desktop/api/wnvapi/ns-wnvapi-wnv_object_change_param">WNV_OBJECT_CHANGE_PARAM</a>



<a href="/windows/desktop/api/wnvapi/ne-wnvapi-wnv_object_type">WNV_OBJECT_TYPE</a>