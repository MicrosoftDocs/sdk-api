---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WNV_PROVIDER_ADDRESS_CHANGE_PARAM structure


## -description


Specifies the provider address's DAD (duplicate address detection) status change, which causes the Windows Network Virtualization (WNV) driver to generate a <b>WnvObjectChangeType</b> notification that specifies the <b>WnvProviderAddressType</b> object type containing this structure.


## -struct-fields




### -field PAFamily

Type: <b>ADDRESS_FAMILY</b>

The address family (<b>AF_INET</b> or <b>AF_INET6</b>) for the provider address.


### -field PA

Type: <b><a href="https://msdn.microsoft.com/1FD137B6-74F4-4E75-A77E-65F093938662">WNV_IP_ADDRESS</a></b>

The IP address object for the provider address, which is the matching IP address used on the physical network for the customer address.


### -field AddressState

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff568758">NL_DAD_STATE</a></b>

A value of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568758">NL_DAD_STATE</a> enumeration that represents the new DAD state. Duplicate address detection is applicable to both IPv4 and IPv6 addresses.

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



For a detailed description of network virtualization concepts and terminology, refer to <a href="http://go.microsoft.com/fwlink/p/?linkid=263545">Hyper-V Network Virtualization Overview</a>.




## -see-also




<a href="https://msdn.microsoft.com/70BE564E-A054-4991-ADCD-79E4D219307B">WNV_NOTIFICATION_TYPE</a>



<a href="https://msdn.microsoft.com/12FF591A-B696-49DF-9E75-B966569A2AAE">WNV_OBJECT_CHANGE_PARAM</a>



<a href="https://msdn.microsoft.com/817C86BB-1267-4174-93C2-515288A33055">WNV_OBJECT_TYPE</a>
 

 

