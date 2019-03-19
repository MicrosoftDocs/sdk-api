---
UID: NF:fwpmu.FwpmNetEventSubscribe0
title: FwpmNetEventSubscribe0 function (fwpmu.h)
author: windows-sdk-content
description: Is used to request the delivery of notifications regarding a particular net event.
old-location: fwp\fwpmneteventsubscribe0.htm
tech.root: fwp
ms.assetid: a2671600-c231-46c8-966d-f444fbdfa944
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FwpmNetEventSubscribe0, FwpmNetEventSubscribe0 function [Filtering], fwp.fwpmneteventsubscribe0, fwpmu/FwpmNetEventSubscribe0
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
 - FwpmNetEventSubscribe0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmNetEventSubscribe0 function


## -description


The <b>FwpmNetEventSubscribe0</b> function  is used to request the delivery of notifications regarding a particular net event.
<div class="alert"><b>Note</b>  <b>FwpmNetEventSubscribe0</b> is the specific implementation of FwpmNetEventSubscribe used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/1e079574-3ab0-48d4-84ab-b2b3f34f757b">FwpmNetEventSubscribe1</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param subscription [in]

Type: <b>const <a href="https://msdn.microsoft.com/a1aa8369-fd70-46f6-983d-0afdf8b8ff77">FWPM_NET_EVENT_SUBSCRIPTION0</a>*</b>

The notifications which will be delivered.


### -param callback [in]

Type: <b><a href="https://msdn.microsoft.com/69b311c5-ac08-490b-823b-4049f7c46975">FWPM_NET_EVENT_CALLBACK0</a></b>

Function pointer that will be invoked when a notification is ready for delivery.


### -param context [in, optional]

Type: <b>void*</b>

Optional context pointer. This pointer is passed to the <i>callback</i> function along with details of the event. 


### -param eventsHandle [out]

Type: <b>HANDLE*</b>

Handle to the newly created subscription.


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
The subscription was created successfully.

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

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_SUBSCRIBE</a> access to the net event's container.




## -see-also




<a href="https://msdn.microsoft.com/69b311c5-ac08-490b-823b-4049f7c46975">FWPM_NET_EVENT_CALLBACK0</a>



<a href="https://msdn.microsoft.com/a1aa8369-fd70-46f6-983d-0afdf8b8ff77">FWPM_NET_EVENT_SUBSCRIPTION0</a>



<a href="https://msdn.microsoft.com/e7d6faba-c280-4867-a9d9-d1bf28e831ef">FwpmNetEventUnsubscribe0</a>
 

 

