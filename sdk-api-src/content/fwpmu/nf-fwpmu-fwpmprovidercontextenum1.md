---
UID: NF:fwpmu.FwpmProviderContextEnum1
title: FwpmProviderContextEnum1 function (fwpmu.h)
description: Returns the next page of results from the provider context enumerator. (FwpmProviderContextEnum1)
helpviewer_keywords: ["FwpmProviderContextEnum1","FwpmProviderContextEnum1 function [Filtering]","fwp.fwpmprovidercontextenum1_func","fwpmu/FwpmProviderContextEnum1"]
old-location: fwp\fwpmprovidercontextenum1_func.htm
tech.root: fwp
ms.assetid: 97a6e562-0423-438d-ab21-48c0f0830610
ms.date: 12/05/2018
ms.keywords: FwpmProviderContextEnum1, FwpmProviderContextEnum1 function [Filtering], fwp.fwpmprovidercontextenum1_func, fwpmu/FwpmProviderContextEnum1
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
 - FwpmProviderContextEnum1
 - fwpmu/FwpmProviderContextEnum1
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
 - FwpmProviderContextEnum1
---

# FwpmProviderContextEnum1 function


## -description

The <b>FwpmProviderContextEnum1</b> function returns the next page of results from the provider context enumerator.
<div class="alert"><b>Note</b>  <b>FwpmProviderContextEnum1</b> is the specific implementation of FwpmProviderContextEnum used in Windows 7. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2">FwpmProviderContextEnum2</a> is available. For Windows Vista, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum0">FwpmProviderContextEnum0</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for a provider context enumeration created by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0">FwpmProviderContextCreateEnumHandle0</a>.

### -param numEntriesRequested [in]

Type: <b>UINT32</b>

The number of provider context objects requested.

### -param entries [out]

Type: [FWPM_PROVIDER_CONTEXT1](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context1)***</b>

The returned provider context objects.

### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of provider context objects returned.

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
The provider contexts were enumerated successfully.

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

<b>FwpmProviderContextEnum1</b> works on a snapshot of the provider contexts taken at the time the enumeration handle was created.

## -see-also

[FWPM_PROVIDER_CONTEXT1](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context1)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0">FwpmProviderContextCreateEnumHandle0</a>
