---
UID: NF:fwpmu.IPsecSaEnum1
title: IPsecSaEnum1 function (fwpmu.h)
description: Returns the next page of results from the IPsec security association (SA) enumerator. (IPsecSaEnum1)
helpviewer_keywords: ["IPsecSaEnum1","IPsecSaEnum1 function [Filtering]","fwp.ipsecsaenum1_func","fwpmu/IPsecSaEnum1"]
old-location: fwp\ipsecsaenum1_func.htm
tech.root: fwp
ms.assetid: 93db625d-9b7f-4038-8c36-dec2762927be
ms.date: 12/05/2018
ms.keywords: IPsecSaEnum1, IPsecSaEnum1 function [Filtering], fwp.ipsecsaenum1_func, fwpmu/IPsecSaEnum1
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IPsecSaEnum1
 - fwpmu/IPsecSaEnum1
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
 - IPsecSaEnum1
---

# IPsecSaEnum1 function


## -description

The <b>IPsecSaEnum1</b> function returns the next page of results from the IPsec security association (SA) enumerator.
<div class="alert"><b>Note</b>  <b>IPsecSaEnum1</b> is the specific implementation of IPsecSaEnum used in Windows 7 and later. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsaenum0">IPsecSaEnum0</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for an IPsec SA enumeration. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacreateenumhandle0">IPsecSaCreateEnumHandle0</a> to obtain an enumeration handle.

### -param numEntriesRequested [in]

Type: <b>UINT32</b>

The number of enumeration entries requested.

### -param entries [out]

Type: [IPSEC_SA_DETAILS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1)***</b>

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

<b>IPsecSaEnum1</b> works on a snapshot of the SAs taken at the time the enumeration handle was created.

## -see-also

[IPSEC_SA_DETAILS1](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacreateenumhandle0">IPsecSaCreateEnumHandle0</a>
