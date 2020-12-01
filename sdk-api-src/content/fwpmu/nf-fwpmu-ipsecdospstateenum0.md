---
UID: NF:fwpmu.IPsecDospStateEnum0
title: IPsecDospStateEnum0 function (fwpmu.h)
description: Returns the next page of results from the IPsec DoS Protection state enumerator. Each IPsec DoS Protection state entry corresponds to a flow that has successfully passed the IPsec DoS Protection authentication checks.
helpviewer_keywords: ["IPsecDospStateEnum0","IPsecDospStateEnum0 function [Filtering]","fwp.ipsecdospstateenum0","fwpmu/IPsecDospStateEnum0"]
old-location: fwp\ipsecdospstateenum0.htm
tech.root: fwp
ms.assetid: d69e323b-249b-4b90-8754-2c910fbc2fc4
ms.date: 12/05/2018
ms.keywords: IPsecDospStateEnum0, IPsecDospStateEnum0 function [Filtering], fwp.ipsecdospstateenum0, fwpmu/IPsecDospStateEnum0
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
 - IPsecDospStateEnum0
 - fwpmu/IPsecDospStateEnum0
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
 - IPsecDospStateEnum0
---

# IPsecDospStateEnum0 function


## -description

The <b>IPsecDospStateEnum0</b> function returns the next page of results from the IPsec DoS Protection state enumerator. Each IPsec DoS Protection state entry corresponds to a flow that has successfully passed the IPsec DoS Protection authentication checks.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for an IPsec DoS Protection enumeration. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecdospstatecreateenumhandle0">IPsecDospStateCreateEnumHandle0</a> to obtain an enumeration handle.

### -param numEntriesRequested [in]

Type: <b>UINT32</b>

The number of enumeration entries requested.

### -param entries [out]

Type: [IPSEC_DOSP_STATE0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_dosp_state0)***</b>

Addresses of the enumeration entries.

### -param numEntries [out]

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
The results   were enumerated successfully.

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

If the <i>numEntries</i> is less than the <i>numEntriesRequested</i>, the enumeration is exhausted.

The returned array of entries (but not the individual entries themselves) must be freed by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

A subsequent call using the same enumeration handle will return the next set of items following those in the last output buffer.

<b>IPsecDospStateEnum0</b> is a specific implementation of IPsecDospStateEnum. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IPSEC_DOSP_STATE0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_dosp_state0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecdospstatecreateenumhandle0">IPsecDospStateCreateEnumHandle0</a>