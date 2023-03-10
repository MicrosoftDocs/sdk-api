---
UID: NF:fwpmu.IPsecSaContextEnum0
title: IPsecSaContextEnum0 function (fwpmu.h)
description: Returns the next page of results from the IPsec security association (SA) context enumerator. (IPsecSaContextEnum0)
helpviewer_keywords: ["IPsecSaContextEnum0","IPsecSaContextEnum0 function [Filtering]","fwp.ipsecsacontextenum0","fwpmu/IPsecSaContextEnum0"]
old-location: fwp\ipsecsacontextenum0.htm
tech.root: fwp
ms.assetid: 67ef4ec6-904b-4b15-a38f-a708448a8646
ms.date: 12/05/2018
ms.keywords: IPsecSaContextEnum0, IPsecSaContextEnum0 function [Filtering], fwp.ipsecsacontextenum0, fwpmu/IPsecSaContextEnum0
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
 - IPsecSaContextEnum0
 - fwpmu/IPsecSaContextEnum0
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
 - IPsecSaContextEnum0
---

# IPsecSaContextEnum0 function


## -description

The <b>IPsecSaContextEnum0</b> function returns the next page of results from the IPsec security association (SA) context enumerator.
<div class="alert"><b>Note</b>  <b>IPsecSaContextEnum0</b> is the specific implementation of IPsecSaContextEnum used in Windows Vista. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextenum1">IPsecSaContextEnum1</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for an SA context enumeration returned by <a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0">IPsecSaContextCreateEnumHandle0</a>.

### -param numEntriesRequested [in]

Type: <b>UINT32</b>

Number of SA contexts requested.

### -param entries [out]

Type: [IPSEC_SA_CONTEXT0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_context0)***</b>

Addresses of the enumeration entries.

### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of SA contexts returned.

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
The IPsec SA contexts were enumerated successfully.

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

## -see-also

[IPSEC_SA_CONTEXT0](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_context0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0">IPsecSaContextCreateEnumHandle0</a>
