---
UID: NF:fwpmu.FwpmTransactionAbort0
title: FwpmTransactionAbort0 function (fwpmu.h)
description: Causes the current transaction within the current session to abort and rollback.
helpviewer_keywords: ["FwpmTransactionAbort0","FwpmTransactionAbort0 function [Filtering]","fwp.fwpmtransactionabort0_func","fwpmu/FwpmTransactionAbort0"]
old-location: fwp\fwpmtransactionabort0_func.htm
tech.root: fwp
ms.assetid: e2574f0c-1070-4e06-8b75-80fa7ec20acf
ms.date: 12/05/2018
ms.keywords: FwpmTransactionAbort0, FwpmTransactionAbort0 function [Filtering], fwp.fwpmtransactionabort0_func, fwpmu/FwpmTransactionAbort0
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
 - FwpmTransactionAbort0
 - fwpmu/FwpmTransactionAbort0
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
 - FwpmTransactionAbort0
---

# FwpmTransactionAbort0 function


## -description

The <b>FwpmTransactionAbort0</b> function causes the current transaction within the current session to abort and rollback.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

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
The transaction was aborted.

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

This function can only be called from within a transaction. Otherwise, it will fail
with <b>FWP_E_NO_TXN_IN_PROGRESS</b>.

<b>FwpmTransactionAbort0</b> is a specific implementation of FwpmTransactionAbort. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmtransactionbegin0">FwpmTransactionBegin0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmtransactioncommit0">FwpmTransactionCommit0</a>