---
UID: NF:fwpmu.FwpmNetEventCreateEnumHandle0
title: FwpmNetEventCreateEnumHandle0 function (fwpmu.h)
description: Creates a handle used to enumerate a set of network events.
helpviewer_keywords: ["FwpmNetEventCreateEnumHandle0","FwpmNetEventCreateEnumHandle0 function [Filtering]","fwp.fwpmneteventcreateenumhandle0","fwpmu/FwpmNetEventCreateEnumHandle0"]
old-location: fwp\fwpmneteventcreateenumhandle0.htm
tech.root: fwp
ms.assetid: 82e0f189-f283-43b2-b9d4-29e754c5c95e
ms.date: 12/05/2018
ms.keywords: FwpmNetEventCreateEnumHandle0, FwpmNetEventCreateEnumHandle0 function [Filtering], fwp.fwpmneteventcreateenumhandle0, fwpmu/FwpmNetEventCreateEnumHandle0
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
 - FwpmNetEventCreateEnumHandle0
 - fwpmu/FwpmNetEventCreateEnumHandle0
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
 - FwpmNetEventCreateEnumHandle0
---

# FwpmNetEventCreateEnumHandle0 function


## -description

The <b>FwpmNetEventCreateEnumHandle0</b> function creates a handle used to enumerate a set of network events.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumTemplate [in, optional]

Type: [FWPM_NET_EVENT_ENUM_TEMPLATE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0)*</b>

  Template to selectively restrict the enumeration.

### -param enumHandle [out]

Type: <b>HANDLE*</b>

The handle for network event enumeration.

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

If <i>enumTemplate</i> is <b>NULL</b>, all network event objects are returned.

The caller must call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventdestroyenumhandle0">FwpmNetEventDestroyEnumHandle0</a> to free the returned handle.

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

The caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_ENUM</a> access to the events' containers. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmNetEventCreateEnumHandle0</b> is a specific implementation of FwpmNetEventCreateEnumHandle. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_NET_EVENT_ENUM_TEMPLATE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventdestroyenumhandle0">FwpmNetEventDestroyEnumHandle0</a>