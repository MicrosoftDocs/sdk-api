---
UID: NF:fwpmu.FwpmNetEventEnum0
title: FwpmNetEventEnum0 function (fwpmu.h)
description: Returns the next page of results from the network event enumerator. (FwpmNetEventEnum0)
helpviewer_keywords: ["FwpmNetEventEnum0","FwpmNetEventEnum0 function [Filtering]","fwp.fwpmneteventenum0","fwpmu/FwpmNetEventEnum0"]
old-location: fwp\fwpmneteventenum0.htm
tech.root: fwp
ms.assetid: c58a273a-c707-47f5-a667-e5d61579d82c
ms.date: 12/05/2018
ms.keywords: FwpmNetEventEnum0, FwpmNetEventEnum0 function [Filtering], fwp.fwpmneteventenum0, fwpmu/FwpmNetEventEnum0
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
 - FwpmNetEventEnum0
 - fwpmu/FwpmNetEventEnum0
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
 - FwpmNetEventEnum0
---

# FwpmNetEventEnum0 function


## -description

The <b>FwpmNetEventEnum0</b> function returns the next page of results from the network event enumerator.
<div class="alert"><b>Note</b>  <b>FwpmNetEventEnum0</b> is the specific implementation of FwpmNetEventEnum used in Windows Vista. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventenum1">FwpmNetEventEnum1</a> is available. For Windows 8, <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventenum2">FwpmNetEventEnum2</a> is available.</div><div> </div>

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle for a network event enumeration created by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0">FwpmNetEventCreateEnumHandle0</a>.

### -param numEntriesRequested [in]

Type: <b>UINT32</b>

The number of enumeration entries requested.

### -param entries [out]

Type: [FWPM_NET_EVENT0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event0)***</b>

Addresses of enumeration entries.

### -param numEntriesReturned [out]

Type: <b>UINT32*</b>

The number of enumeration entries returned.

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
The network events were enumerated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_NET_EVENTS_DISABLED</b></dt>
<dt>0x80320013</dt>
</dl>
</td>
<td width="60%">
The collection of network diagnostic events is disabled.
Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmenginesetoption0">FwpmEngineSetOption0</a> to enable it.

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

A subsequent call  that uses  the same <i>enumHandle</i> parameter will return the next set of events following those in the  current <i>entries</i> buffer.

<b>FwpmNetEventEnum0</b> returns only events that were logged prior to the creation of the  <i>enumHandle</i> parameter. See <a href="/windows/desktop/FWP/logging">Logging</a> for more information.

## -see-also

[FWPM_NET_EVENT0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event0)



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0">FwpmNetEventCreateEnumHandle0</a>



<a href="/windows/desktop/FWP/logging">WFP Logging</a>
