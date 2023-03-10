---
UID: NF:fwpmu.FwpmFilterDeleteById0
title: FwpmFilterDeleteById0 function (fwpmu.h)
description: Removes a filter object from the system. (FwpmFilterDeleteById0)
helpviewer_keywords: ["FwpmFilterDeleteById0","FwpmFilterDeleteById0 function [Filtering]","fwp.fwpmfilterdeletebyid0_func","fwpmu/FwpmFilterDeleteById0"]
old-location: fwp\fwpmfilterdeletebyid0_func.htm
tech.root: fwp
ms.assetid: a1b10a05-27e9-49f3-8e1c-30650007a9ef
ms.date: 12/05/2018
ms.keywords: FwpmFilterDeleteById0, FwpmFilterDeleteById0 function [Filtering], fwp.fwpmfilterdeletebyid0_func, fwpmu/FwpmFilterDeleteById0
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
 - FwpmFilterDeleteById0
 - fwpmu/FwpmFilterDeleteById0
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
 - FwpmFilterDeleteById0
---

# FwpmFilterDeleteById0 function


## -description

The <b>FwpmFilterDeleteById0</b> function removes a filter object from the system.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param id [in]

Type: <b>UINT64</b>

Runtime identifier for the object  being removed from the system. This value is returned by the  <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfilteradd0">FwpmFilterAdd0</a> function.

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
The filter was successfully deleted.

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

The caller needs <a href="/windows/desktop/SecAuthZ/standard-access-rights">DELETE</a> access to the filter. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmFilterDeleteById0</b> is a specific implementation of FwpmFilterDeleteById. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfilteradd0">FwpmFilterAdd0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfiltergetbyid0">FwpmFilterGetById0</a>
