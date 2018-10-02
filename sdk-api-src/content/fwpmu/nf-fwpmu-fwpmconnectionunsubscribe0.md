---
UID: NF:fwpmu.FwpmConnectionUnsubscribe0
title: FwpmConnectionUnsubscribe0 function
author: windows-sdk-content
description: Is used to cancel a connection object change event subscription and stop receiving notifications.
old-location: fwp\fwpmconnectionunsubscribe0.htm
tech.root: FWP
ms.assetid: b9fc4c7f-5cbd-4c85-9317-2aa027d3bcde
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FwpmConnectionUnsubscribe0, FwpmConnectionUnsubscribe0 function [Filtering], fwp.fwpmconnectionunsubscribe0, fwpmu/FwpmConnectionUnsubscribe0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmConnectionUnsubscribe0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmConnectionUnsubscribe0 function


## -description


The <b>FwpmConnectionUnsubscribe0</b> function is used to cancel a connection object  change event subscription and stop receiving notifications.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param eventsHandle [in, out]

Type: <b>HANDLE</b>

Handle of the subscribed event notification. This is the returned handle from the call to <a href="https://msdn.microsoft.com/86fe40b0-aada-44e1-91dd-0e825589159d">FwpmConnectionSubscribe0</a>.

This may be <b>NULL</b>, in which case the function will have no effect.


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
The subscription was deleted successfully.

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



If the callback is currently being invoked, this function will not return until it completes. Thus, when calling this function, you must not hold any locks that the callback may also try to acquire lest you deadlock. 

It is not necessary to unsubscribe before closing a session; all subscriptions are automatically canceled when the subscribing session terminates.

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.




## -see-also




<a href="https://msdn.microsoft.com/86fe40b0-aada-44e1-91dd-0e825589159d">FwpmConnectionSubscribe0</a>
 

 

