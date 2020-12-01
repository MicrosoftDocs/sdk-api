---
UID: NF:fwpmu.FwpmProviderAdd0
title: FwpmProviderAdd0 function (fwpmu.h)
description: Adds a new provider to the system.
helpviewer_keywords: ["FwpmProviderAdd0","FwpmProviderAdd0 function [Filtering]","fwp.fwpmprovideradd0_func","fwpmu/FwpmProviderAdd0"]
old-location: fwp\fwpmprovideradd0_func.htm
tech.root: fwp
ms.assetid: e76f03e2-0853-465a-9f82-c29d35de32c9
ms.date: 12/05/2018
ms.keywords: FwpmProviderAdd0, FwpmProviderAdd0 function [Filtering], fwp.fwpmprovideradd0_func, fwpmu/FwpmProviderAdd0
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
 - FwpmProviderAdd0
 - fwpmu/FwpmProviderAdd0
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
 - FwpmProviderAdd0
---

# FwpmProviderAdd0 function


## -description

The <b>FwpmProviderAdd0</b> function   adds a new provider to the system.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param provider [in]

Type: [FWPM_PROVIDER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider0)*</b>

The provider object to be added.

### -param sd [in, optional]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">PSECURITY_DESCRIPTOR</a></b>

Security information for the provider object.

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
The provider was successfully added.

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

If the caller supplies a null security descriptor, the system will assign a default security descriptor.

Boot-time objects are added to the Base Filtering Engine (BFE) when the TCP/IP driver starts, and are removed once the BFE finishes initialization.  Persistent objects are added when the BFE starts. If a policy provider has a persistent policy that is not intended to be enforced if its associated service is disabled, the caller can specify an optional service name in the [FWPM_PROVIDER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider0) structure.  This service then owns the persistent policy object.  At start, the BFE only adds the following types of persistent objects to the system.

<ul>
<li>The object is not associated with a provider.</li>
<li>The object has an associated provider that does not specify a service name.</li>
<li>The object has an associated provider and an associated service set to auto-start.</li>
</ul>
This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD</a> access to the provider's container.  See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmProviderAdd0</b> is a specific implementation of FwpmProviderAdd. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_PROVIDER0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider0)