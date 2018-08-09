---
UID: NF:fwpmu.FwpmCalloutUnsubscribeChanges0
title: FwpmCalloutUnsubscribeChanges0 function
author: windows-sdk-content
description: Is used to cancel a callout change subscription and stop receiving change notifications.
old-location: fwp\fwpmcalloutunsubscribechanges0_func.htm
old-project: fwp
ms.assetid: ab0825fc-edf8-4634-a6bb-86de7e1e030c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FwpmCalloutUnsubscribeChanges0, FwpmCalloutUnsubscribeChanges0 function [Filtering], fwp.fwpmcalloutunsubscribechanges0_func, fwpmu/FwpmCalloutUnsubscribeChanges0
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmCalloutUnsubscribeChanges0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmCalloutUnsubscribeChanges0 function


## -description


The <b>FwpmCalloutUnsubscribeChanges0</b> function is used to cancel a callout change subscription and stop receiving change notifications.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param changeHandle [in]

Type: <b>HANDLE</b>

Handle of the subscribed change notification. This is the handle returned by the call to <a href="https://msdn.microsoft.com/1460603c-6897-4559-b376-b87a6c2f4309">FwpmCalloutSubscribeChanges0</a>.


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



If the callback is currently being invoked, this function will not return until the callback completes. Thus, when calling this function, you must not hold any locks that the callback may also try to acquire lest you deadlock. 

It is not necessary to unsubscribe before closing a session; all subscriptions are automatically canceled when the subscribing session terminates.

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

<b>FwpmCalloutUnsubscribeChanges0</b> is a specific implementation of FwpmCalloutUnsubscribeChanges. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/1460603c-6897-4559-b376-b87a6c2f4309">FwpmCalloutSubscribeChanges0</a>
 

 

