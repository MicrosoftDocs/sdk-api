---
UID: NF:fwpmu.FwpmCalloutAdd0
title: FwpmCalloutAdd0 function (fwpmu.h)
description: Adds a new callout object to the system.
helpviewer_keywords: ["FwpmCalloutAdd0","FwpmCalloutAdd0 function [Filtering]","fwp.fwpmcalloutadd0_func","fwpmu/FwpmCalloutAdd0"]
old-location: fwp\fwpmcalloutadd0_func.htm
tech.root: fwp
ms.assetid: e4f79262-6345-49e9-a50c-9f8a82f2df0e
ms.date: 12/05/2018
ms.keywords: FwpmCalloutAdd0, FwpmCalloutAdd0 function [Filtering], fwp.fwpmcalloutadd0_func, fwpmu/FwpmCalloutAdd0
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
 - FwpmCalloutAdd0
 - fwpmu/FwpmCalloutAdd0
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
 - FwpmCalloutAdd0
---

# FwpmCalloutAdd0 function


## -description

The <b>FwpmCalloutAdd0</b> function adds a new callout object to the system.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param callout [in]

Type: [FWPM_CALLOUT0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_callout0)*</b>

The callout object to be added.

### -param sd [in, optional]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">PSECURITY_DESCRIPTOR</a></b>

The security information associated with the callout.

### -param id [out, optional]

Type: <b>UINT32*</b>

Runtime identifier for this callout.

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
The callout was successfully added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_INVALID_PARAMETER</b></dt>
<dt>0x80320035</dt>
</dl>
</td>
<td width="60%">
FWPM_TUNNEL_FLAG_POINT_TO_POINT was not set and conditions other than local/remote
   address were specified.

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

Some fields in the [FWPM_CALLOUT0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_callout0) structure are assigned by the system, not the caller, and are ignored in the call to <b>FwpmCalloutAdd0</b>. If the caller supplies a null security descriptor, the system will assign a default security descriptor.

This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ADD</a> access to the callout's container, 
   <b>FWPM_ACTRL_ADD_LINK </b> access to the provider (if any), and 
   <b>FWPM_ACTRL_ADD_LINK </b> access to the applicable layer. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

To add a filter that references a callout, invoke the functions in the following order.

<ul>
<li>Call <a href="/windows-hardware/drivers/ddi/fwpsk/nf-fwpsk-fwpscalloutregister0">FwpsCalloutRegister</a> (documented in the Windows Driver Kit (WDK)), to register the callout with the filter engine.</li>
<li>Call <b>FwpmCalloutAdd0</b> to add the callout to the system.</li>
<li>Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfilteradd0">FwpmFilterAdd0</a> to add the filter that references the callout to the system.</li>
</ul>
  
By default filters that reference callouts that have been added but have not yet registered with the filter engine are treated as Block filters.

<b>FwpmCalloutAdd0</b> is a specific implementation of FwpmCalloutAdd. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_CALLOUT0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_callout0)



<a href="/windows-hardware/drivers/ddi/fwpmk/nf-fwpmk-fwpmcalloutadd0">Kernel-Mode FwpmCalloutAdd0</a>