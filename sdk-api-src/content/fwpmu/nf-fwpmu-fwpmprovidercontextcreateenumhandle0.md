---
UID: NF:fwpmu.FwpmProviderContextCreateEnumHandle0
title: FwpmProviderContextCreateEnumHandle0 function (fwpmu.h)
description: Creates a handle used to enumerate a set of provider contexts.
helpviewer_keywords: ["FwpmProviderContextCreateEnumHandle0","FwpmProviderContextCreateEnumHandle0 function [Filtering]","fwp.fwpmprovidercontextcreateenumhandle0_func","fwpmu/FwpmProviderContextCreateEnumHandle0"]
old-location: fwp\fwpmprovidercontextcreateenumhandle0_func.htm
tech.root: fwp
ms.assetid: 3b660e3a-fba6-4466-aa82-eb90c27ae004
ms.date: 12/05/2018
ms.keywords: FwpmProviderContextCreateEnumHandle0, FwpmProviderContextCreateEnumHandle0 function [Filtering], fwp.fwpmprovidercontextcreateenumhandle0_func, fwpmu/FwpmProviderContextCreateEnumHandle0
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
 - FwpmProviderContextCreateEnumHandle0
 - fwpmu/FwpmProviderContextCreateEnumHandle0
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
 - FwpmProviderContextCreateEnumHandle0
---

# FwpmProviderContextCreateEnumHandle0 function


## -description

The <b>FwpmProviderContextCreateEnumHandle0</b> function creates a handle used to enumerate a set of provider contexts.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumTemplate [in, optional]

Type: <b>const <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a>*</b>

Template to selectively restrict the enumeration.

### -param enumHandle [out]

Type: <b>HANDLE*</b>

Handle for provider context enumeration.

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
The enumerator was created successfully.

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

If <i>enumTemplate</i> is <b>NULL</b>, all provider contexts are returned.

The enumerator is not "live", meaning it does not reflect changes made to the system after the call to  <b>FwpmProviderContextCreateEnumHandle0</b> returns. If you need to ensure that the results are current, you must call <b>FwpmProviderContextCreateEnumHandle0</b> and <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum0">FwpmProviderContextEnum0</a> from within the same explicit transaction.

The caller must free the returned handle by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextdestroyenumhandle0">FwpmProviderContextDestroyEnumHandle0</a>.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ENUM</a> access to the provider contexts' containers and <b>FWPM_ACTRL_READ</b> access to the provider contexts. Only provider contexts to which the caller has <b>FWPM_ACTRL_READ</b> access will be returned. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmProviderContextCreateEnumHandle0</b> is a specific implementation of FwpmProviderContextCreateEnumHandle. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextdestroyenumhandle0">FwpmProviderContextDestroyEnumHandle0</a>