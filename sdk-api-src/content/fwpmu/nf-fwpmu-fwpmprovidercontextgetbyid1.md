---
UID: NF:fwpmu.FwpmProviderContextGetById1
title: FwpmProviderContextGetById1 function (fwpmu.h)
description: Retrieves a provider context. (FwpmProviderContextGetById1)
helpviewer_keywords: ["FwpmProviderContextGetById1","FwpmProviderContextGetById1 function [Filtering]","fwp.fwpmprovidercontextgetbyid1_func","fwpmu/FwpmProviderContextGetById1"]
old-location: fwp\fwpmprovidercontextgetbyid1_func.htm
tech.root: fwp
ms.assetid: 76353efa-844e-4c7f-9f9a-0bf2e247c58b
ms.date: 12/05/2018
ms.keywords: FwpmProviderContextGetById1, FwpmProviderContextGetById1 function [Filtering], fwp.fwpmprovidercontextgetbyid1_func, fwpmu/FwpmProviderContextGetById1
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
 - FwpmProviderContextGetById1
 - fwpmu/FwpmProviderContextGetById1
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
 - FwpmProviderContextGetById1
---

# FwpmProviderContextGetById1 function


## -description

The <b>FwpmProviderContextGetById1</b> function retrieves a provider context.
<div class="alert"><b>Note</b>  <b>FwpmProviderContextGetById1</b> is the specific implementation of FwpmProviderContextGetById used in Windows 7. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2">FwpmProviderContextGetById2</a> is available. For Windows Vista, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid0">FwpmProviderContextGetById0</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

A run-time identifier for the desired object. This must be the run-time identifier that was received from the system when the application called <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd1">FwpmProviderContextAdd1</a> for this object.

### -param providerContext [out]

Type: [FWPM_PROVIDER_CONTEXT1](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context1)**</b>

The provider context information.

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
The provider context was retrieved successfully.

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

The caller must free the returned object by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_READ</a> access to the provider context. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

## -see-also

[FWPM_PROVIDER_CONTEXT1](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context1)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd1">FwpmProviderContextAdd1</a>
