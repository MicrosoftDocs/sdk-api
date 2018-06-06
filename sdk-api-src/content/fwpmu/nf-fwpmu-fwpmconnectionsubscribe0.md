---
UID: NF:fwpmu.FwpmConnectionSubscribe0
title: FwpmConnectionSubscribe0 function
author: windows-sdk-content
description: Is used to request the delivery of notifications about changes to a connection object.
old-location: fwp\fwpmconnectionsubscribe0.htm
old-project: FWP
ms.assetid: 86fe40b0-aada-44e1-91dd-0e825589159d
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: FwpmConnectionSubscribe0, FwpmConnectionSubscribe0 function [Filtering], fwp.fwpmconnectionsubscribe0, fwpmu/FwpmConnectionSubscribe0
ms.prod: windows
ms.technology: windows-sdk
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
 - FwpmConnectionSubscribe0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmConnectionSubscribe0 function


## -description


The <b>FwpmConnectionSubscribe0</b> function is used to request the delivery of notifications about changes to a connection object.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param subscription [in]

Type: <b>const <a href="https://msdn.microsoft.com/020490f1-ccbe-41aa-b6ad-022be9c9bef4">FWPM_CONNECTION_SUBSCRIPTION0</a>*</b>

The notifications which will be delivered.


### -param callback [in]

Type: <b><a href="https://msdn.microsoft.com/92aac379-6145-4556-a4cd-6a27fda4d910">FWPM_CONNECTION_CALLBACK0</a></b>

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

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_SUBSCRIBE</a> access to the connection object's container.




## -see-also




<a href="https://msdn.microsoft.com/92aac379-6145-4556-a4cd-6a27fda4d910">FWPM_CONNECTION_CALLBACK0</a>



<a href="https://msdn.microsoft.com/020490f1-ccbe-41aa-b6ad-022be9c9bef4">FWPM_CONNECTION_SUBSCRIPTION0</a>



<a href="https://msdn.microsoft.com/b9fc4c7f-5cbd-4c85-9317-2aa027d3bcde">FwpmConnectionUnsubscribe0</a>
 

 

