---
UID: NF:fwpmu.FwpmNetEventEnum4
title: FwpmNetEventEnum4
description: Retrieves the next page of results from the network event enumerator.
tech.root: fwp
ms.date: 05/01/2024
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
 - FwpmNetEventEnum4
f1_keywords:
 - FwpmNetEventEnum4
 - fwpmu/FwpmNetEventEnum4
dev_langs:
 - c++
helpviewer_keywords:
 - FwpmNetEventEnum4
---

## -description

Retrieves the next page of results from the network event enumerator.

## -parameters

### -param engineHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to an open session with the filter engine. To open a session with the filter engine, call [FwpmEngineOpen0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineopen0).

### -param enumHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to a network event enumeration created by a call to [FwpmNetEventCreateEnumHandle0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0).

### -param numEntriesRequested

Type: \_In\_ **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of enumeration entries requested.

### -param entries

Type: \_Outptr\_result\_buffer\_\(*numEntriesReturned\) **const [FWPM_NET_EVENT4](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event4)\*\*\***

Addresses of enumeration entries.

### -param numEntriesReturned

Type: \_Out\_ **[UINT32](/windows/win32/winprog/windows-data-types)\***

The number of enumeration entries returned.

## -returns

|Return code/value|Description|
|-|-|
|ERROR_SUCCESS<br/>0|The network events were enumerated successfully.|
|FWP_E_NET_EVENTS_DISABLED<br/>0x80320013|The collection of network diagnostic events is disabled.
Call [FwpmEngineSetOption0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmenginesetoption0) to enable it.|
|FWP_E_* error code<br/>0x80320001—0x80320039|A Windows Filtering Platform (WFP)-specific error. For details, see [WFP error codes](/windows/win32/fwp/wfp-error-codes).|
|RPC_* error code<br/>0x80010001—0x80010122|Failure to communicate with the remote or local firewall engine.|

## -remarks

If *numEntriesReturned* is less than the *numEntriesRequested*, then the enumeration is exhausted.

You must free the returned array of entries (but not the individual entries themselves) by calling [FwpmFreeMemory0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmfreememory0).

A subsequent call that uses the same *enumHandle* parameter will return the next set of events following those in the current *entries* buffer.

**FwpmNetEventEnum4** returns only events that were logged prior to the creation of the *enumHandle* parameter. For more info, see [Logging](/windows/win32/fwp/logging).

## -see-also
