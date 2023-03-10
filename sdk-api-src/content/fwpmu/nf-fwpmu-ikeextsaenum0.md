---
UID: NF:fwpmu.IkeextSaEnum0
title: IkeextSaEnum0 function (fwpmu.h)
description: Returns the next page of results from the IKE/AuthIP security association (SA) enumerator. (IkeextSaEnum0)
helpviewer_keywords: ["IkeextSaEnum0","IkeextSaEnum0 function [Filtering]","fwp.ikeextsaenum0","fwpmu/IkeextSaEnum0"]
old-location: fwp\ikeextsaenum0.htm
tech.root: fwp
ms.assetid: a38e266d-2155-4dd4-b12e-5f1a40ca776e
ms.date: 12/05/2018
ms.keywords: IkeextSaEnum0, IkeextSaEnum0 function [Filtering], fwp.ikeextsaenum0, fwpmu/IkeextSaEnum0
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
 - IkeextSaEnum0
 - fwpmu/IkeextSaEnum0
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
 - IkeextSaEnum0
---

# IkeextSaEnum0 function


## -description

The <b>IkeextSaEnum0</b> function returns the next page of results from the IKE/AuthIP security association (SA) enumerator.
<div class="alert"><b>Note</b>  <b>IkeextSaEnum0</b> is the specific implementation of IkeextSaEnum used in Windows Vista. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ikeextsaenum1">IkeextSaEnum1</a> is available. For Windows 8, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ikeextsaenum2">IkeextSaEnum2</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for an IKE/AuthIP SA enumeration. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ikeextsacreateenumhandle0">IkeextSaCreateEnumHandle0</a> to obtain an enumeration handle.

### -param numEntriesRequested [in]

Type: <b>UINT32</b>

Number of enumeration entries requested.

### -param entries [out]

Type: [IKEEXT_SA_DETAILS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details0)***</b>

Addresses of the enumeration entries.

### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of enumeration entries returned.

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
The SAs were enumerated successfully.

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

<b>IkeextSaEnum0</b> works on a snapshot of the SAs taken at the time the enumeration handle was created.

## -see-also

<a href="/windows/desktop/FWP/fwp-ike-functions">IKE/AuthIP Functions</a>



[IKEEXT_SA_DETAILS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_sa_details0)



<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>
