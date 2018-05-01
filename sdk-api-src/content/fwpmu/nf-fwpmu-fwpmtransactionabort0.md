---
UID: NF:fwpmu.FwpmTransactionAbort0
title: FwpmTransactionAbort0 function
author: windows-driver-content
description: Causes the current transaction within the current session to abort and rollback.
old-location: fwp\fwpmtransactionabort0_func.htm
old-project: FWP
ms.assetid: e2574f0c-1070-4e06-8b75-80fa7ec20acf
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: FwpmTransactionAbort0, FwpmTransactionAbort0 function [Filtering], fwp.fwpmtransactionabort0_func, fwpmu/FwpmTransactionAbort0
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	FwpmTransactionAbort0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmTransactionAbort0 function


## -description


The <b>FwpmTransactionAbort0</b> function causes the current transaction within the current session to abort and rollback.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call  <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


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



This function can only be called from within a transaction. Otherwise, it will fail
with <b>FWP_E_NO_TXN_IN_PROGRESS</b>.

<b>FwpmTransactionAbort0</b> is a specific implementation of FwpmTransactionAbort. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/9eaf1101-7cf3-4eb2-9ca0-47108a5c80c7">FwpmTransactionBegin0</a>



<a href="https://msdn.microsoft.com/3bde803c-f416-4096-98c5-1c56e4a86b94">FwpmTransactionCommit0</a>
 

 

