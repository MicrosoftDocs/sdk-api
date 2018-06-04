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

# FWP_CLASSIFY_OPTION_TYPE_ enumeration


## -description


The <b>FWP_CLASSIFY_OPTION_TYPE</b> enumerated type is used by callouts and shims during run-time classification.

<b>FWP_CLASSIFY_OPTION_TYPE</b> specifies timeout options for unicast, multicast, and loose source mapping states and enables blocking or permission of state creation on outbound multicast and broadcast traffic.


## -enum-fields




### -field FWP_CLASSIFY_OPTION_MULTICAST_STATE

Specifies the multicast conditions on outbound traffic. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff550078">FWPM_CLASSIFY_OPTION0</a> for possible values.


### -field FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING

Specifies the source mapping conditions for callout filters. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff550078">FWPM_CLASSIFY_OPTION0</a> for possible values.

 Loose source mapping allows unicast responses from a remote peer to match only the port number, instead of the entire source address.


### -field FWP_CLASSIFY_OPTION_UNICAST_LIFETIME

Specifies the unicast state lifetime, in seconds.


### -field FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME

Specifies the multicast/broadcast state lifetime, in seconds.


### -field FWP_CLASSIFY_OPTION_SECURE_SOCKET_SECURITY_FLAGS

Specifies that the callout can set secure socket settings on the endpoint.    Such flags are only allowed to increase the overall security level. The possible values are defined in the <i>Mstcpip.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SOCKET_SETTINGS_GUARANTEE_ENCRYPTION 0x00000001 </td>
<td>Indicates that guaranteed encryption of traffic is required.  This flag should be set if the default policy prefers methods of protection that do not use encryption. If this flag is set and encryption is not possible for any reason, no packets will be sent and a connection will not be established.</td>
</tr>
<tr>
<td>SOCKET_SETTINGS_ALLOW_INSECURE 0x00000002 </td>
<td>Indicates that clear text connections are allowed.  If this flag is set, some or all of the sent packets will be sent in clear text, especially if security with the peer could not be negotiated.<div class="alert"><b>Note</b>  If this flag is not set, it is guaranteed that packets will never be sent in clear text, even if security negotiation fails.</div>
<div> </div>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Available only in Windows 7,  Windows Server 2008 R2, and later.</div>
<div> </div>

### -field FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_MM_POLICY_KEY

Allows the callout to specify the specific main mode (MM) policy used for the connection.   

<div class="alert"><b>Note</b>  Available only in Windows 7,  Windows Server 2008 R2, and later.</div>
<div> </div>

### -field FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_QM_POLICY_KEY

Allows the callout to specify the specific quick mode (QM) policy used for the connection.   

<div class="alert"><b>Note</b>  Available only in Windows 7,  Windows Server 2008 R2, and later.</div>
<div> </div>

### -field FWP_CLASSIFY_OPTION_LOCAL_ONLY_MAPPING


### -field FWP_CLASSIFY_OPTION_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550078">FWPM_CLASSIFY_OPTION0</a>
 

 

