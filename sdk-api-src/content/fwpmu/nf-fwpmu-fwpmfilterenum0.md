---
UID: NF:fwpmu.FwpmFilterEnum0
title: FwpmFilterEnum0 function (fwpmu.h)
description: Returns the next page of results from the filter enumerator.
helpviewer_keywords: ["FwpmFilterEnum0","FwpmFilterEnum0 function [Filtering]","fwp.fwpmfilterenum0_func","fwpmu/FwpmFilterEnum0"]
old-location: fwp\fwpmfilterenum0_func.htm
tech.root: fwp
ms.assetid: ced06ffd-668f-4d2b-b727-b705ad6a3149
ms.date: 12/05/2018
ms.keywords: FwpmFilterEnum0, FwpmFilterEnum0 function [Filtering], fwp.fwpmfilterenum0_func, fwpmu/FwpmFilterEnum0
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmFilterEnum0
 - fwpmu/FwpmFilterEnum0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmFilterEnum0
---

# FwpmFilterEnum0 function


## -description

The <b>FwpmFilterEnum0</b> function returns the next page of results from the filter enumerator.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for a filter enumeration created by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0">FwpmFilterCreateEnumHandle0</a>.

### -param numEntriesRequested [in]

Type: <b>UINT32</b>

The number of filter objects requested.

### -param entries [out]

Type: [FWPM_FILTER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)***</b>

Addresses of enumeration entries.

### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of filter objects returned.

## -returns

Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The filters were enumerated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>

## -remarks

If the <i>numEntriesReturned</i> is less than the <i>numEntriesRequested</i>, the enumeration is exhausted. 

The returned array of entries (but not the individual entries themselves) must be freed by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

A subsequent call using the same enumeration handle will return the next set of items following those in the last output buffer.

<b>FwpmFilterEnum0</b> works on a snapshot of the filters taken at the time the enumeration handle was created.

<b>FwpmFilterEnum0</b> is a specific implementation of FwpmFilterEnum. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_FILTER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_filter0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0">FwpmFilterCreateEnumHandle0</a>