---
UID: NF:fwpmu.FwpmProviderContextAdd2
title: FwpmProviderContextAdd2 function (fwpmu.h)
description: Adds a new provider context to the system. (FwpmProviderContextAdd2)
helpviewer_keywords: ["FwpmProviderContextAdd2","FwpmProviderContextAdd2 function [Filtering]","fwp.fwpmprovidercontextadd2","fwpmu/FwpmProviderContextAdd2"]
old-location: fwp\fwpmprovidercontextadd2.htm
tech.root: fwp
ms.assetid: 07c6b1fc-55bb-4526-a24b-0e22f147e5cc
ms.date: 12/05/2018
ms.keywords: FwpmProviderContextAdd2, FwpmProviderContextAdd2 function [Filtering], fwp.fwpmprovidercontextadd2, fwpmu/FwpmProviderContextAdd2
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - FwpmProviderContextAdd2
 - fwpmu/FwpmProviderContextAdd2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - fwpuclnt.dll
api_name:
 - FwpmProviderContextAdd2
---

## -description

The <b>FwpmProviderContextAdd2</b> function adds a new provider context to the system.
<div class="alert"><b>Note</b>  <b>FwpmProviderContextAdd2</b> is the specific implementation of FwpmProviderContextAdd used in Windows 8. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd1">FwpmProviderContextAdd1</a> is available. For Windows Vista, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd0">FwpmProviderContextAdd0</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param providerContext [in]

Type: **[FWPM_PROVIDER_CONTEXT2](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)\***

The provider context object to be added.

### -param sd [in, optional]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">PSECURITY_DESCRIPTOR</a></b>

Security information associated with the provider context object.

### -param id [out, optional]

Type: <b>UINT64*</b>

Pointer to a variable that receives a runtime identifier for this provider context.

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
The provider context was successfully added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
<dt>0x32</dt>
</dl>
</td>
<td width="60%">
The [FWPM_IPSEC_IKE_MM_CONTEXT](/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)and     the [IKEEXT_IPV6_CGA](/windows/desktop/api/iketypes/ne-iketypes-ikeext_authentication_method_type) authentication method in the <b>authenticationMethods</b> array, but cryptographically generated address (CGA) is not enabled in
      the registry.

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

Some fields in the [FWPM_PROVIDER_CONTEXT2](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2) structure are assigned by the system, not the caller, and are ignored in the call to <b>FwpmProviderContextAdd2</b>. 

If the caller supplies a <b>NULL</b> security descriptor, the system will assign a default security descriptor.

This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD</a> access to the provider context's container and <b>FWPM_ACTRL_ADD_LINK</b> access to the provider (if any).  See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

## -see-also

[FWPM_PROVIDER_CONTEXT2](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
