---
UID: NF:fwpmu.FwpmSystemPortsUnsubscribe0
title: FwpmSystemPortsUnsubscribe0 function
author: windows-sdk-content
description: Is used to cancel a system port subscription and stop receiving notifications.
old-location: fwp\fwpmsystemportsunsubscribe0.htm
tech.root: fwp
ms.assetid: d078ae73-32a7-4341-b142-d1fdf8388255
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: FwpmSystemPortsUnsubscribe0, FwpmSystemPortsUnsubscribe0 function [Filtering], fwp.fwpmsystemportsunsubscribe0, fwpmu/FwpmSystemPortsUnsubscribe0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - FwpmSystemPortsUnsubscribe0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmSystemPortsUnsubscribe0 function


## -description


The <b>FwpmSystemPortsUnsubscribe0</b> function is used to cancel a system port subscription and stop receiving notifications.


## -parameters




### -param engineHandle [in, optional]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param sysPortsHandle [in, out]

Type: <b>HANDLE</b>

Handle of the subscribed system port notification. This is the returned handle from the call to <a href="https://msdn.microsoft.com/e0eecf0e-e6b2-4df9-8a8e-766ee5c8189f">FwpmSystemPortsSubscribe0</a>.


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



Unsubscribing with an invalid object handle will result in a return value of ERROR_SUCCESS, but the actual subscription will persist until the unsubscribe API is called with valid parameters.

If the callback is currently being invoked, this function will not return until it completes. Thus, when calling this function, you must not hold any locks that the callback may also try to acquire lest you deadlock.

It is not necessary to unsubscribe before closing a session; all subscriptions are automatically canceled when the subscribing session terminates.

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

<b>FwpmSystemPortsUnsubscribe0</b> is a specific implementation of FwpmSystemPortsUnsubscribe. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e0eecf0e-e6b2-4df9-8a8e-766ee5c8189f">FwpmSystemPortsSubscribe0</a>
 

 

