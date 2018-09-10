---
UID: NF:fwpmu.FwpmTransactionBegin0
title: FwpmTransactionBegin0 function
author: windows-sdk-content
description: Begins an explicit transaction within the current session.
old-location: fwp\fwpmtransactionbegin0_func.htm
tech.root: fwp
ms.assetid: 9eaf1101-7cf3-4eb2-9ca0-47108a5c80c7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FWPM_TXN_READ_ONLY, FwpmTransactionBegin0, FwpmTransactionBegin0 function [Filtering], fwp.fwpmtransactionbegin0_func, fwpmu/FwpmTransactionBegin0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmTransactionBegin0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmTransactionBegin0 function


## -description


The <b>FwpmTransactionBegin0</b> function begins an explicit transaction within the current session.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


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
A Windows Filtering Platform (WFP) specific error. See <a href="https://msdn.microsoft.com/11f3085a-f044-4a78-b47a-59b9086562bf">WFP Error Codes</a> for details.

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
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

For a read-only transaction, the caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_BEGIN_READ_TXN</a> access to the filter engine. For a read/write transaction, the caller needs <b>FWPM_ACTRL_BEGIN_WRITE_TXN</b> access to the filter engine. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmTransactionBegin0</b> is a specific implementation of FwpmTransactionBegin. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.


#### Examples

The following C++ example illustrates wrapping the <a href="https://msdn.microsoft.com/ca11187e-3a91-438f-9a7f-606da7c88f6d">FwpmFilterAdd0</a> function in an FWP transaction.


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




<a href="https://msdn.microsoft.com/e2574f0c-1070-4e06-8b75-80fa7ec20acf">FwpmTransactionAbort0</a>



<a href="https://msdn.microsoft.com/3bde803c-f416-4096-98c5-1c56e4a86b94">FwpmTransactionCommit0</a>
 

 

