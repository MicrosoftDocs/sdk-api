---
UID: NF:fwpmu.FwpmConnectionDestroyEnumHandle0
title: FwpmConnectionDestroyEnumHandle0 function (fwpmu.h)
description: Frees a handle returned by FwpmConnectionCreateEnumHandle0.
helpviewer_keywords: ["FwpmConnectionDestroyEnumHandle0","FwpmConnectionDestroyEnumHandle0 function [Filtering]","fwp.fwpmconnectiondestroyenumhandle0","fwpmu/FwpmConnectionDestroyEnumHandle0"]
old-location: fwp\fwpmconnectiondestroyenumhandle0.htm
tech.root: fwp
ms.assetid: 0325908e-4d2b-4cdb-9cfa-f2985a76dba9
ms.date: 12/05/2018
ms.keywords: FwpmConnectionDestroyEnumHandle0, FwpmConnectionDestroyEnumHandle0 function [Filtering], fwp.fwpmconnectiondestroyenumhandle0, fwpmu/FwpmConnectionDestroyEnumHandle0
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
 - FwpmConnectionDestroyEnumHandle0
 - fwpmu/FwpmConnectionDestroyEnumHandle0
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
 - FwpmConnectionDestroyEnumHandle0
---

# FwpmConnectionDestroyEnumHandle0 function


## -description

The <b>FwpmConnectionDestroyEnumHandle0</b> function frees a handle returned by <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0">FwpmConnectionCreateEnumHandle0</a>.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param enumHandle [in]

Type: <b>HANDLE</b>

Handle of a connection object enumeration created by a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0">FwpmProviderContextCreateEnumHandle0</a>.

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

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0">FwpmConnectionCreateEnumHandle0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0">FwpmProviderContextCreateEnumHandle0</a>