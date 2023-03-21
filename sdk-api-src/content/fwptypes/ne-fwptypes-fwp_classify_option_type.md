---
UID: NE:fwptypes.FWP_CLASSIFY_OPTION_TYPE_
title: FWP_CLASSIFY_OPTION_TYPE (fwptypes.h)
description: The FWP_CLASSIFY_OPTION_TYPE enumerated type is used by callouts and shims during run-time classification.FWP_CLASSIFY_OPTION_TYPE specifies timeout options for unicast, multicast, and loose source mapping states and enables blocking or permission of state creation on outbound multicast and broadcast traffic.
helpviewer_keywords: ["FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING","FWP_CLASSIFY_OPTION_MAX","FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME","FWP_CLASSIFY_OPTION_MULTICAST_STATE","FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_MM_POLICY_KEY","FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_QM_POLICY_KEY","FWP_CLASSIFY_OPTION_SECURE_SOCKET_SECURITY_FLAGS","FWP_CLASSIFY_OPTION_TYPE","FWP_CLASSIFY_OPTION_TYPE enumeration [Filtering]","FWP_CLASSIFY_OPTION_UNICAST_LIFETIME","fwp.fwp_classify_option_type","fwptypes/FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING","fwptypes/FWP_CLASSIFY_OPTION_MAX","fwptypes/FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME","fwptypes/FWP_CLASSIFY_OPTION_MULTICAST_STATE","fwptypes/FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_MM_POLICY_KEY","fwptypes/FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_QM_POLICY_KEY","fwptypes/FWP_CLASSIFY_OPTION_SECURE_SOCKET_SECURITY_FLAGS","fwptypes/FWP_CLASSIFY_OPTION_TYPE","fwptypes/FWP_CLASSIFY_OPTION_UNICAST_LIFETIME"]
old-location: fwp\fwp_classify_option_type.htm
tech.root: fwp
ms.assetid: 5c757bf6-a4ea-42f0-ad87-74855703a041
ms.date: 12/05/2018
ms.keywords: FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING, FWP_CLASSIFY_OPTION_MAX, FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME, FWP_CLASSIFY_OPTION_MULTICAST_STATE, FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_MM_POLICY_KEY, FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_QM_POLICY_KEY, FWP_CLASSIFY_OPTION_SECURE_SOCKET_SECURITY_FLAGS, FWP_CLASSIFY_OPTION_TYPE, FWP_CLASSIFY_OPTION_TYPE enumeration [Filtering], FWP_CLASSIFY_OPTION_UNICAST_LIFETIME, fwp.fwp_classify_option_type, fwptypes/FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING, fwptypes/FWP_CLASSIFY_OPTION_MAX, fwptypes/FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME, fwptypes/FWP_CLASSIFY_OPTION_MULTICAST_STATE, fwptypes/FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_MM_POLICY_KEY, fwptypes/FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_QM_POLICY_KEY, fwptypes/FWP_CLASSIFY_OPTION_SECURE_SOCKET_SECURITY_FLAGS, fwptypes/FWP_CLASSIFY_OPTION_TYPE, fwptypes/FWP_CLASSIFY_OPTION_UNICAST_LIFETIME
req.header: fwptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwptypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWP_CLASSIFY_OPTION_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWP_CLASSIFY_OPTION_TYPE_
 - fwptypes/FWP_CLASSIFY_OPTION_TYPE_
 - FWP_CLASSIFY_OPTION_TYPE
 - fwptypes/FWP_CLASSIFY_OPTION_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwptypes.h
api_name:
 - FWP_CLASSIFY_OPTION_TYPE
---

# FWP_CLASSIFY_OPTION_TYPE enumeration


## -description

The <b>FWP_CLASSIFY_OPTION_TYPE</b> enumerated type is used by callouts and shims during run-time classification.

<b>FWP_CLASSIFY_OPTION_TYPE</b> specifies timeout options for unicast, multicast, and loose source mapping states and enables blocking or permission of state creation on outbound multicast and broadcast traffic.

## -enum-fields

### -field FWP_CLASSIFY_OPTION_MULTICAST_STATE:0

Specifies the multicast conditions on outbound traffic. See [FWPM_CLASSIFY_OPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) for possible values.

### -field FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING

Specifies the source mapping conditions for callout filters. See [FWPM_CLASSIFY_OPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) for possible values.

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

[FWPM_CLASSIFY_OPTION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_classify_option0)
