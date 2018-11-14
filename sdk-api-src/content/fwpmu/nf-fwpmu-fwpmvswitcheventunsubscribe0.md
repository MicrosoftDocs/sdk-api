---
UID: NF:fwpmu.FwpmvSwitchEventUnsubscribe0
title: FwpmvSwitchEventUnsubscribe0 function
author: windows-sdk-content
description: Is used to cancel a vSwitch event subscription and stop receiving notifications.
old-location: fwp\fwpmvswitcheventunsubscribe0.htm
tech.root: fwp
ms.assetid: adc258b4-c4ee-4ff8-8174-42c58377ea32
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FwpmvSwitchEventUnsubscribe0, FwpmvSwitchEventUnsubscribe0 function [Filtering], fwp.fwpmvswitcheventunsubscribe0, fwpmu/FwpmvSwitchEventUnsubscribe0
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
 - FwpmvSwitchEventUnsubscribe0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FwpmvSwitchEventUnsubscribe0
: 
---

# FwpmvSwitchEventUnsubscribe0 function


## -description


The <b>FwpmvSwitchEventUnsubscribe0</b> function is used to cancel a vSwitch event subscription and stop receiving notifications.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param subscriptionHandle [in, out]

Type: <b>HANDLE</b>

Handle of the subscribed event notification. This is the returned handle from the call to <a href="https://msdn.microsoft.com/1264a58d-81e1-4877-915d-6ed3d7d15512">FwpmvSwitchEventSubscribe0</a>.

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

<b>FwpmvSwitchEventUnsubscribe0</b> is a specific implementation of FwpmvSwitchEventUnsubscribe. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/1264a58d-81e1-4877-915d-6ed3d7d15512">FwpmvSwitchEventSubscribe0</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

