---
UID: NF:fwpmu.FwpmProviderContextDeleteByKey0
title: FwpmProviderContextDeleteByKey0 function (fwpmu.h)
description: Removes a provider context from the system.
helpviewer_keywords: ["FwpmProviderContextDeleteByKey0","FwpmProviderContextDeleteByKey0 function [Filtering]","fwp.fwpmprovidercontextdeletebykey0_func","fwpmu/FwpmProviderContextDeleteByKey0"]
old-location: fwp\fwpmprovidercontextdeletebykey0_func.htm
tech.root: fwp
ms.assetid: 453ab1f7-d137-4252-9445-7195624a5465
ms.date: 12/05/2018
ms.keywords: FwpmProviderContextDeleteByKey0, FwpmProviderContextDeleteByKey0 function [Filtering], fwp.fwpmprovidercontextdeletebykey0_func, fwpmu/FwpmProviderContextDeleteByKey0
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
 - FwpmProviderContextDeleteByKey0
 - fwpmu/FwpmProviderContextDeleteByKey0
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
 - FwpmProviderContextDeleteByKey0
---

# FwpmProviderContextDeleteByKey0 function


## -description

The <b>FwpmProviderContextDeleteByKey0</b> function removes a provider context from the system.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of the object being removed from the system. This is a pointer to the same GUID that was specified when the application called <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd0">FwpmProviderContextAdd0</a> for this object.

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
The provider context was successfully deleted.

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

This function cannot be called from within a read-only transaction. It will fail with
<b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

This function can be called within a dynamic session if the corresponding object was added during the same session. If this function is called for an object that was added during a different dynamic session, it will fail with <b>FWP_E_WRONG_SESSION</b>. If this function is called for an object that was not added during a dynamic session, it will fail with <b>FWP_E_DYNAMIC_SESSION_IN_PROGRESS</b>.

The caller needs <a href="/windows/desktop/SecAuthZ/standard-access-rights">DELETE</a> access to the provider context. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmProviderContextDeleteByKey0</b> is a specific implementation of FwpmProviderContextDeleteByKey. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd0">FwpmProviderContextAdd0</a>