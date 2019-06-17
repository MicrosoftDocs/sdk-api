---
UID: NS:fwpmtypes.FWPM_CONNECTION0_
title: FWPM_CONNECTION0 (fwpmtypes.h)
author: windows-sdk-content
description: Stores the state associated with a connection object.
old-location: fwp\fwpm_connection0.htm
tech.root: fwp
ms.assetid: 76a923d4-57a9-47ba-af91-ee33c3c5b34b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_CONNECTION0, FWPM_CONNECTION0 structure [Filtering], fwp.fwpm_connection0, fwpmtypes/FWPM_CONNECTION0
ms.topic: struct
f1_keywords: ["fwpmtypes/FWPM_CONNECTION0"]
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
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
 - Fwpmtypes.h
api_name:
 - FWPM_CONNECTION0
product: Windows
targetos: Windows
req.typenames: FWPM_CONNECTION0
req.redist: 
ms.custom: 19H1
---

# FWPM_CONNECTION0 structure


## -description


The <b>FWPM_CONNECTION0</b> structure stores the state associated with a connection object.


## -struct-fields




### -field connectionId

Type: <b>UINT64</b>

The run-time identifier for the connection.


### -field ipVersion

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version_">FWP_IP_VERSION</a></b>

The IP version being used. 


### -field localV4Address

Type: <b>UINT32</b>

The IPv4 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field localV6Address

Type: <b>UINT8[16]</b>

The IPv6 local address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field remoteV4Address

Type: <b>UINT32</b>

The IPv4 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field remoteV6Address

Type: <b>UINT8[16]</b>

The IPv6 remote address.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V6</b>.


### -field providerKey

Type: <b>GUID*</b>

Uniquely identifies the provider associated with this connection. 


### -field ipsecTrafficModeType

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_traffic_type_">IPSEC_TRAFFIC_TYPE</a></b>

The type of IPsec traffic.


### -field keyModuleType

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_key_module_type_">IKEEXT_KEY_MODULE_TYPE</a></b>

The type of keying module.


### -field mmCrypto

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_proposal0_">IKEEXT_PROPOSAL0</a></b>

An IKE/AuthIP main mode proposal.


### -field mmPeer

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential2_">IKEEXT_CREDENTIAL2</a></b>

Main mode credential information.


### -field emPeer

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential2_">IKEEXT_CREDENTIAL2</a></b>

Extended mode credential information.


### -field bytesTransferredIn

Type: <b>UINT64</b>

The total number of incoming bytes transferred by the connection.


### -field bytesTransferredOut

Type: <b>UINT64</b>

The total number of outgoing bytes transferred by the connection.


### -field bytesTransferredTotal

Type: <b>UINT64</b>

The total number of bytes (incoming and outgoing) transferred by the connection.


### -field startSysTime

Type: <b>FILETIME</b>

Time that the connection was created.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwptypes/ne-fwptypes-fwp_ip_version_">FWP_IP_VERSION</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential2_">IKEEXT_CREDENTIAL2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ne-iketypes-ikeext_key_module_type_">IKEEXT_KEY_MODULE_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_proposal0_">IKEEXT_PROPOSAL0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ne-ipsectypes-ipsec_traffic_type_">IPSEC_TRAFFIC_TYPE</a>
 

 

