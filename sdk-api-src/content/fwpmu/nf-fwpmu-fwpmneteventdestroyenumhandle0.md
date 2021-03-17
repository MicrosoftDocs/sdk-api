---
UID: NF:fwpmu.FwpmNetEventDestroyEnumHandle0
title: FwpmNetEventDestroyEnumHandle0 function (fwpmu.h)
description: Frees a handle returned by FwpmNetEventCreateEnumHandle0.
helpviewer_keywords: ["FwpmNetEventDestroyEnumHandle0","FwpmNetEventDestroyEnumHandle0 function [Filtering]","fwp.fwpmneteventdestroyenumhandle0","fwpmu/FwpmNetEventDestroyEnumHandle0"]
old-location: fwp\fwpmneteventdestroyenumhandle0.htm
tech.root: fwp
ms.assetid: c9a0b31b-28f2-4f55-8a08-5fea182f8954
ms.date: 12/05/2018
ms.keywords: FwpmNetEventDestroyEnumHandle0, FwpmNetEventDestroyEnumHandle0 function [Filtering], fwp.fwpmneteventdestroyenumhandle0, fwpmu/FwpmNetEventDestroyEnumHandle0
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
 - FwpmNetEventDestroyEnumHandle0
 - fwpmu/FwpmNetEventDestroyEnumHandle0
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
 - FwpmNetEventDestroyEnumHandle0
---

# FwpmNetEventDestroyEnumHandle0 function


## -description

The <b>FwpmNetEventDestroyEnumHandle0</b> function frees a handle returned by <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0">FwpmNetEventCreateEnumHandle0</a>.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle of a network event enumeration created by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0">FwpmNetEventCreateEnumHandle0</a>.

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
The enumerator was successfully deleted.

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

<b>FwpmNetEventDestroyEnumHandle0</b> is a specific implementation of FwpmNetEventDestroyEnumHandle. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0">FwpmNetEventCreateEnumHandle0</a>