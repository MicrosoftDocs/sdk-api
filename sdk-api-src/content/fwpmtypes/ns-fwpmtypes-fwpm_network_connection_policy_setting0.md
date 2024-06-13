---
UID: NS:fwpmtypes.FWPM_NETWORK_CONNECTION_POLICY_SETTING0_
title: FWPM_NETWORK_CONNECTION_POLICY_SETTING0
description: Stores a type and value pair for a connection policy setting.
tech.root: fwp
ms.date: 04/26/2024
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: fwpmtypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: FWPM_NETWORK_CONNECTION_POLICY_SETTING0
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpmtypes.h
api_name:
 - FWPM_NETWORK_CONNECTION_POLICY_SETTING0_
 - FWPM_NETWORK_CONNECTION_POLICY_SETTING0
f1_keywords:
 - FWPM_NETWORK_CONNECTION_POLICY_SETTING0_
 - fwpmtypes/FWPM_NETWORK_CONNECTION_POLICY_SETTING0_
 - FWPM_NETWORK_CONNECTION_POLICY_SETTING0
 - fwpmtypes/FWPM_NETWORK_CONNECTION_POLICY_SETTING0
dev_langs:
 - c++
helpviewer_keywords:
 - FWPM_NETWORK_CONNECTION_POLICY_SETTING0_
---

## -description

Stores a type and value pair for a connection policy setting. You use this structure with [FwpmConnectionPolicyAdd0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmconnectionpolicyadd0).

## -struct-fields

### -field type

A type of connection policy setting. See [FWP_NETWORK_CONNECTION_POLICY_SETTING_TYPE](/windows/win32/api/fwptypes/ne-fwptypes-fwp_network_connection_policy_setting_type).

### -field value

The value of a connection policy setting.

**FWP_NETWORK_CONNECTION_POLICY_SOURCE_ADDRESS**. The source address to use for the connection. The value should be a **FWP_UINT32** for an IPv4 address, and a **FWP_BYTE_ARRAY16_TYPE** for an IPv6 address.
 
**FWP_NETWORK_CONNECTION_POLICY_NEXT_HOP_INTERFACE**. The LUID of the outgoing interface to use for the connection. The value should be a **FWP_UINT64**.
 
**FWP_NETWORK_CONNECTION_POLICY_NEXT_HOP**. The nexthop address (or gateway) to use for the connection. The value should be a **FWP_UINT32** for an IPv4 address, and a **FWP_BYTE_ARRAY16_TYPE** for an IPv6 address.          

## -remarks

## -see-also
