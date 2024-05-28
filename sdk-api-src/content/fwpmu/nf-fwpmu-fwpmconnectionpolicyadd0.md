---
UID: NF:fwpmu.FwpmConnectionPolicyAdd0
title: FwpmConnectionPolicyAdd0
description: Allows you to configure expressive routing policies for outbound connections.
tech.root: fwp
ms.date: 04/29/2024
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Fwpuclnt.dll
req.header: fwpmu.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Fwpuclnt.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmConnectionPolicyAdd0
f1_keywords:
 - FwpmConnectionPolicyAdd0
 - fwpmu/FwpmConnectionPolicyAdd0
dev_langs:
 - c++
helpviewer_keywords:
 - FwpmConnectionPolicyAdd0
---

## -description

The TCP/IP stack supports destination address-based routing for outbound connections. **FwpmConnectionPolicyAdd0API** allows you to configure more expressive routing policies for outbound connections, and thereby to enable more complex scenarios such as source address-based routing, process-based routing, port-based routing, and others. A connection policy consists of an array of match conditions, an array of route settings, and an associated weight. You can configure multiple policies, and they are evaluated based on their configured weights for an outbound connection (a higher weight takes precedence). The route setting of the first policy whose conditions (ANDed) matches the outbound connection is applied.

## -parameters

### -param engineHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to an open session with the filter engine. To open a session with the filter engine, call [FwpmEngineOpen0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineopen0).

### -param connectionPolicy

Type: \_In\_ **const [FWPM_PROVIDER_CONTEXT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3)\***

The state associated with a provider context.

### -param ipVersion

Type: \_In\_ **[FWP_IP_VERSION](/windows/win32/api/fwptypes/ne-fwptypes-fwp_ip_version)**

IP version of the traffic.

### -param weight

Type: \_In\_ **[UINT64](/windows/win32/winprog/windows-data-types)**

Specifies the weight that this Trusted Intermediary Agent (TIA) should be given compared to any peers.

### -param numFilterConditions

Type: \_In\_ **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of elements in *filterConditions*.

### -param filterConditions

Type: \_In\_reads\_\(numFilterConditions\) **const [FWPM_FILTER_CONDITION0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)\***

A filter condition that must be true for the action to be taken.

Of the possible match conditions (see [Filtering condition identifiers](/windows/win32/fwp/filtering-condition-identifiers-)), the ones in the following list are supported by **FwpmConnectionPolicyAdd0**. Set these values in **FWPM_FILTER_CONDITION0::fieldKey**.

* **FWPM_CONDITION_ALE_APP_ID**
* **FWPM_CONDITION_ALE_USER_ID**
* **FWPM_CONDITION_IP_LOCAL_ADDRESS**
* **FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE**
* **FWPM_CONDITION_IP_LOCAL_PORT**
* **FWPM_CONDITION_IP_PROTOCOL**
* **FWPM_CONDITION_IP_REMOTE_ADDRESS**
* **FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE**
* **FWPM_CONDITION_IP_REMOTE_PORT**   
* **FWPM_CONDITION_FLAGS**
* **FWPM_CONDITION_ALE_ORIGINAL_APP_ID**
* **FWPM_CONDITION_ALE_PACKAGE_ID**
* **FWPM_CONDITION_COMPARTMENT_ID**

### -param sd

Type: \_In\_opt\_ **[PSECURITY_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor)**

The security information.

## -returns

## -remarks

These are the supported route settings (see [FWP_NETWORK_CONNECTION_POLICY_SETTING_TYPE](/windows/win32/api/fwptypes/ne-fwptypes-fwp_network_connection_policy_setting_type)):

**FWP_NETWORK_CONNECTION_POLICY_SOURCE_ADDRESS**. The source address to use for the connection. The value should be a **FWP_UINT32** for an IPv4 address, and a **FWP_BYTE_ARRAY16_TYPE** for an IPv6 address.

**FWP_NETWORK_CONNECTION_POLICY_NEXT_HOP_INTERFACE**. The LUID of the outgoing interface to use for the connection. The value should be a **FWP_UINT64**.
 
**FWP_NETWORK_CONNECTION_POLICY_NEXT_HOP**. The nexthop address (or gateway) to use for the connection. The value should be a **FWP_UINT32** for an IPv4 address, and a **FWP_BYTE_ARRAY16_TYPE** for an IPv6 address.          

## -see-also
