---
UID: NF:fwpmu.FwpmIPsecTunnelAdd3
title: FwpmIPsecTunnelAdd3
description: Adds a new Internet Protocol Security (IPsec) tunnel mode policy to the system.
tech.root: fwp
ms.date: 04/30/2024
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
 - FwpmIPsecTunnelAdd3
f1_keywords:
 - FwpmIPsecTunnelAdd3
 - fwpmu/FwpmIPsecTunnelAdd3
dev_langs:
 - c++
helpviewer_keywords:
 - FwpmIPsecTunnelAdd3
---

## -description

Adds a new Internet Protocol Security (IPsec) tunnel mode policy to the system.

## -parameters

### -param engineHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to an open session with the filter engine. To open a session with the filter engine, call [FwpmEngineOpen0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineopen0).

### -param flags

Type: \_In\_ **[UINT32](/windows/win32/winprog/windows-data-types)**

Possible values:

|IPsec tunnel flag|Meaning|
|-|-|
|FWPM_TUNNEL_FLAG_POINT_TO_POINT|Adds a point-to-point tunnel to the system.|
|FWPM_TUNNEL_FLAG_ENABLE_VIRTUAL_IF_TUNNELING|Enables virtual interface-based IPsec tunnel mode.|

### -param mainModePolicy

Type: \_In\_opt\_ **const [FWPM_PROVIDER_CONTEXT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3)\***

An optional Main Mode policy for the IPsec tunnel.

### -param tunnelPolicy

Type: \_In\_ **const [FWPM_PROVIDER_CONTEXT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3)\***

The Quick Mode policy for the IPsec tunnel.

### -param numFilterConditions

Type: \_In\_ **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of filter conditions present in *filterConditions*.

### -param filterConditions

Type: \_In\_reads\_\(numFilterConditions\) **const [FWPM_FILTER_CONDITION0](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)\***

An array of filter conditions that describe the traffic that should be tunneled by IPsec.

### -param keyModKey

Type: \_In\_opt\_ **const [GUID](/windows/win32/api/guiddef/ns-guiddef-guid)\***

An optional pointer to a GUID that uniquely identifies the keying module key. If you supply this parameter, then only that keying module will be used for the tunnel. Otherwise, the default keying policy applies.

### -param sd

Type: \_In\_opt\_ **[PSECURITY_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor)**

The security information associated with the IPsec tunnel.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)**

|Return code/value|Description|
|-|-|
|ERROR_SUCCESS<br/>0|The IPsec tunnel mode policy was successfully added.|
|FWP_E_INVALID_PARAMETER<br/>0x80320035|FWPM_TUNNEL_FLAG_POINT_TO_POINT wasn't set, and conditions other than local/remote address were specified.|
|FWP_E_* error code<br/>0x80320001—0x80320039|A Windows Filtering Platform (WFP)-specific error. For details, see [WFP error codes](/windows/win32/fwp/wfp-error-codes).|
|RPC_* error code<br/>0x80010001—0x80010122|Failure to communicate with the remote or local firewall engine.|

## -remarks

You can't call this function within a read-only transaction. It will fail with **FWP_E_INCOMPATIBLE_TXN**. For more info about transactions, see [Object management](/windows/win32/fwp/object-management).

## -see-also
