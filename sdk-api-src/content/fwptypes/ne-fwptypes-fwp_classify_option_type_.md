---
UID: NE:fwptypes.FWP_CLASSIFY_OPTION_TYPE_
title: FWP_CLASSIFY_OPTION_TYPE_
author: windows-sdk-content
description: The FWP_CLASSIFY_OPTION_TYPE enumeration type specifies time-out options for unicast, multicast, and loose source mapping states and enables blocking or permission of state creation on outbound multicast and broadcast traffic.
old-location: netvista\fwp_classify_option_type.htm
tech.root: NetVista
ms.assetid: 4731b03d-4c51-414b-a07d-0957b9a04db2
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING, FWP_CLASSIFY_OPTION_MAX, FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME, FWP_CLASSIFY_OPTION_MULTICAST_STATE, FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_MM_POLICY_KEY, FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_QM_POLICY_KEY, FWP_CLASSIFY_OPTION_SECURE_SOCKET_SECURITY_FLAGS, FWP_CLASSIFY_OPTION_TYPE, FWP_CLASSIFY_OPTION_TYPE enumeration [Network Drivers Starting with Windows Vista], FWP_CLASSIFY_OPTION_TYPE_, FWP_CLASSIFY_OPTION_UNICAST_LIFETIME, fwptypes/FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING, fwptypes/FWP_CLASSIFY_OPTION_MAX, fwptypes/FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME, fwptypes/FWP_CLASSIFY_OPTION_MULTICAST_STATE, fwptypes/FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_MM_POLICY_KEY, fwptypes/FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_QM_POLICY_KEY, fwptypes/FWP_CLASSIFY_OPTION_SECURE_SOCKET_SECURITY_FLAGS, fwptypes/FWP_CLASSIFY_OPTION_TYPE, fwptypes/FWP_CLASSIFY_OPTION_UNICAST_LIFETIME, netvista.fwp_classify_option_type, wfp_ref_4_enum_f92482a5-f10c-4e89-be92-e2b706f2dfd8.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: fwptypes.h
req.include-header: Fwpsk.h
req.target-type: Windows
req.target-min-winverclnt: Supported starting with Windows Vista.
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwptypes.h
api_name:
 - FWP_CLASSIFY_OPTION_TYPE
product: Windows
targetos: Windows
req.typenames: FWP_CLASSIFY_OPTION_TYPE
req.redist: 
---

# FWP_CLASSIFY_OPTION_TYPE_ enumeration


## -description


The FWP_CLASSIFY_OPTION_TYPE enumeration type specifies time-out options for unicast, multicast, and
  loose source mapping states and enables blocking or permission of state creation on outbound multicast and
  broadcast traffic.


## -enum-fields




### -field FWP_CLASSIFY_OPTION_MULTICAST_STATE

Indicates that a multicast state is to be treated in a particular manner.


### -field FWP_CLASSIFY_OPTION_LOOSE_SOURCE_MAPPING

Indicates that loose source mapping settings need to be applied for the current non-TCP
     connection. This option allows unicast responses from a remote peer to match only the port number, not
     the source address.


### -field FWP_CLASSIFY_OPTION_UNICAST_LIFETIME

Indicates a modification to the lifetime of a unicast state for any traffic that matches this
     filter, ranging from its default (60 seconds) to some other value, in seconds.


### -field FWP_CLASSIFY_OPTION_MCAST_BCAST_LIFETIME

Indicates a modification to the lifetime of a multicast and broadcast state for any traffic that
     matches this filter, from its default (3 seconds) to some other value, in seconds.


### -field FWP_CLASSIFY_OPTION_SECURE_SOCKET_SECURITY_FLAGS

A bitmask that indicates the secure socket settings that a callout function can set on the endpoint.
      These settings are only allowed to increase the overall security level

This bitmask is specified through a bitwise OR of the following flags, which are defined in 
      <i>Mstcpip.h</i>:





#### SOCKET_SETTINGS_GUARANTEE_ENCRYPTION

Indicates that guaranteed encryption of traffic is required. This flag should be set if the
        default policy prefers methods of protection that do not use encryption. If this flag is set and
        encryption is not possible for any reason, no packets will be sent and a connection will not be
        established.



#### SOCKET_SETTINGS_ALLOW_INSECURE

Indicates that clear text connections are allowed. If this flag is set, some or all of the sent
         packets will be sent in clear text, especially if security with the peer could not be
         negotiated.

<div class="alert"><b>Note</b>  If this flag is not set, packets will never be sent in clear text, even if
         security negotiation fails.</div>
<div> </div>
<div class="alert"><b>Note</b>  Available only in Windows 7 and Windows Server 2008 R2.</div>
<div> </div>

### -field FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_MM_POLICY_KEY

Indicates that a callout function is allowed to specify the specific main mode (MM) policy used for
      the connection.

<div class="alert"><b>Note</b>  Available only in Windows 7 and Windows Server 2008 R2.</div>
<div> </div>

### -field FWP_CLASSIFY_OPTION_SECURE_SOCKET_AUTHIP_QM_POLICY_KEY

Indicates that a callout function is allowed to specify the specific quick mode (QM) policy used for
      the connection.

<div class="alert"><b>Note</b>  Available only in Windows 7 and Windows Server 2008 R2.</div>
<div> </div>

### -field FWP_CLASSIFY_OPTION_LOCAL_ONLY_MAPPING


### -field FWP_CLASSIFY_OPTION_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
     header files and binaries.

