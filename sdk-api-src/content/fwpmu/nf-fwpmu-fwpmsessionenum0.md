---
UID: NF:fwpmu.FwpmSessionEnum0
title: FwpmSessionEnum0 function (fwpmu.h)
description: Returns the next page of results from the session enumerator.
helpviewer_keywords: ["FwpmSessionEnum0","FwpmSessionEnum0 function [Filtering]","fwp.fwpmsessionenum0_func","fwpmu/FwpmSessionEnum0"]
old-location: fwp\fwpmsessionenum0_func.htm
tech.root: fwp
ms.assetid: fb67d74a-dd96-434c-b218-a34ca6043cb1
ms.date: 12/05/2018
ms.keywords: FwpmSessionEnum0, FwpmSessionEnum0 function [Filtering], fwp.fwpmsessionenum0_func, fwpmu/FwpmSessionEnum0
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
 - FwpmSessionEnum0
 - fwpmu/FwpmSessionEnum0
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
 - FwpmSessionEnum0
---

# FwpmSessionEnum0 function


## -description

The <b>FwpmSessionEnum0</b> function returns the next page of results from the session enumerator.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for a session enumeration created by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0">FwpmSessionCreateEnumHandle0</a>.

### -param numEntriesRequested [in]

Type: <b>UINT32</b>

The number of session entries requested.

### -param entries [out]

Type: [FWPM_SESSION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_session0)***</b>

Addresses of the enumeration entries.

### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of session objects returned.

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
The sessions were enumerated successfully.

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

<b>FwpmSessionEnum0</b> works on a snapshot of the sessions taken at the time the enumeration handle was created.

<b>FwpmSessionEnum0</b> is a specific implementation of FwpmSessionEnum. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_SESSION0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_session0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0">FwpmSessionCreateEnumHandle0</a>