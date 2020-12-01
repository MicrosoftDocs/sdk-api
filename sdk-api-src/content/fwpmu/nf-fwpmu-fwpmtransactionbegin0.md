---
UID: NF:fwpmu.FwpmTransactionBegin0
title: FwpmTransactionBegin0 function (fwpmu.h)
description: Begins an explicit transaction within the current session.
helpviewer_keywords: ["FWPM_TXN_READ_ONLY","FwpmTransactionBegin0","FwpmTransactionBegin0 function [Filtering]","fwp.fwpmtransactionbegin0_func","fwpmu/FwpmTransactionBegin0"]
old-location: fwp\fwpmtransactionbegin0_func.htm
tech.root: fwp
ms.assetid: 9eaf1101-7cf3-4eb2-9ca0-47108a5c80c7
ms.date: 12/05/2018
ms.keywords: FWPM_TXN_READ_ONLY, FwpmTransactionBegin0, FwpmTransactionBegin0 function [Filtering], fwp.fwpmtransactionbegin0_func, fwpmu/FwpmTransactionBegin0
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
 - FwpmTransactionBegin0
 - fwpmu/FwpmTransactionBegin0
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
 - FwpmTransactionBegin0
---

# FwpmTransactionBegin0 function


## -description

The <b>FwpmTransactionBegin0</b> function begins an explicit transaction within the current session.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param flags [in]

Type: <b>UINT32</b>

Possible values:

<table>
<tr>
<th>Transaction flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Begin read/write transaction.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_TXN_READ_ONLY"></a><a id="fwpm_txn_read_only"></a><dl>
<dt><b>FWPM_TXN_READ_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Begin read-only transaction.

</td>
</tr>
</table>

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
The transaction was started successfully.

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

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

For a read-only transaction, the caller needs <a href="/windows/desktop/FWP/access-right-identifiers">FWPM_ACTRL_BEGIN_READ_TXN</a> access to the filter engine. For a read/write transaction, the caller needs <b>FWPM_ACTRL_BEGIN_WRITE_TXN</b> access to the filter engine. See <a href="/windows/desktop/FWP/access-control">Access Control</a> for more information.

<b>FwpmTransactionBegin0</b> is a specific implementation of FwpmTransactionBegin. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example illustrates wrapping the <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfilteradd0">FwpmFilterAdd0</a> function in an FWP transaction.


```cpp
#include <windows.h>
#include <fwpmu.h>
#include <stdio.h>

#pragma comment(lib, "Fwpuclnt.lib")

void main()
{
    HANDLE engineHandle = NULL; 

    FWPM_FILTER0      fwpFilter;

    RtlZeroMemory(&fwpFilter, sizeof(FWPM_FILTER0));
    fwpFilter.layerKey = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4;
    fwpFilter.action.type = FWP_ACTION_BLOCK;
    fwpFilter.weight.type = FWP_EMPTY;
    fwpFilter.numFilterConditions = 0;

    DWORD  result = ERROR_SUCCESS; 
    DWORD fwpTxStatus = ERROR_SUCCESS;

    printf("Opening filter engine.\n");
    result = FwpmEngineOpen0(NULL, RPC_C_AUTHN_WINNT, NULL, NULL, &engineHandle);
      if (result != ERROR_SUCCESS)
      {            
        printf("FwpmEngineOpen0 failed (%d).\n", result);
        return;
    }
             
      printf("Adding filter to permit traffic for Application 1.\n");
      fwpTxStatus = FwpmTransactionBegin0(engineHandle, NULL);
      if (fwpTxStatus != ERROR_SUCCESS)
      {            
        printf("FwpmTransactionBegin0 failed (%d).\n", fwpTxStatus);
        return;
    }

    result = FwpmFilterAdd0(engineHandle, &fwpFilter, NULL, NULL);
      if (result != ERROR_SUCCESS)
      {            
        printf("FwpmFilterAdd0 failed (%d).\n", result);
        return;
    }

    result = FwpmTransactionCommit0(engineHandle);
    if (result != ERROR_SUCCESS)
    {            
        printf("FwpmTransactionCommit0 failed (%d).\n", result);
        return;
    }
    else
    {
        printf("Filter transaction (adding a filter) committed successfully.\n");
    }

    return;
}
// ----------------------------------------------------------------------

```

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmtransactionabort0">FwpmTransactionAbort0</a>



<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmtransactioncommit0">FwpmTransactionCommit0</a>