---
UID: NF:fwpmu.FwpmProviderContextEnum3
title: FwpmProviderContextEnum3
description: Returns the next page of results from the provider context enumerator.
tech.root: fwp
ms.date: 05/02/2024
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
 - FwpmProviderContextEnum3
f1_keywords:
 - FwpmProviderContextEnum3
 - fwpmu/FwpmProviderContextEnum3
dev_langs:
 - c++
helpviewer_keywords:
 - FwpmProviderContextEnum3
---

## -description

Returns the next page of results from the provider context enumerator.

## -parameters

### -param engineHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to an open session with the filter engine. To open a session with the filter engine, call [FwpmEngineOpen0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineopen0).

### -param enumHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to a network event enumeration created by a call to [FwpmProviderContextCreateEnumHandle0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0).

### -param numEntriesRequested

Type: \_In\_ **[UINT32](/windows/win32/winprog/windows-data-types)**

Number of provider context objects requested.

### -param entries

Type: \_Outptr\_result\_buffer\_\(*numEntriesReturned\) **[FWPM_PROVIDER_CONTEXT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3)\*\*\***

The returned provider context objects.

### -param numEntriesReturned

Type: \_Out\_ **[UINT32](/windows/win32/winprog/windows-data-types)\***

The number of provider context objects returned.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)\***

|Return code/value|Description|
|-|-|
|ERROR_SUCCESS<br/>0|The provider contexts were enumerated successfully.|
|FWP_E_* error code<br/>0x80320001—0x80320039|A Windows Filtering Platform (WFP)-specific error. For details, see [WFP error codes](/windows/win32/fwp/wfp-error-codes).|
|RPC_* error code<br/>0x80010001—0x80010122|Failure to communicate with the remote or local firewall engine.|

## -remarks

If *numEntriesReturned* is less than the *numEntriesRequested*, then the enumeration is exhausted.

You must free the returned array of entries (but not the individual entries themselves) by calling [FwpmFreeMemory0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmfreememory0).

A subsequent call that uses the same *enumHandle* parameter will return the next set of events following those in the last output buffer.

**FwpmProviderContextEnum3** works on a snapshot of the provider contexts taken at the time the enumeration handle was created.

## -see-also
