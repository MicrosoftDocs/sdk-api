---
UID: NF:fwpmu.FwpmFilterSubscribeChanges0
title: FwpmFilterSubscribeChanges0 function
author: windows-sdk-content
description: Is used to request the delivery of notifications regarding changes in a particular filter.
old-location: fwp\fwpmfiltersubscribechanges0_func.htm
old-project: fwp
ms.assetid: 6dafce5d-239f-44b6-a24b-2b5646bfe4ec
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FwpmFilterSubscribeChanges0, FwpmFilterSubscribeChanges0 function [Filtering], fwp.fwpmfiltersubscribechanges0_func, fwpmu/FwpmFilterSubscribeChanges0
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
 - FwpmFilterSubscribeChanges0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmFilterSubscribeChanges0 function


## -description


The <b>FwpmFilterSubscribeChanges0</b> function  is used to request the delivery of notifications regarding changes in a particular filter.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param subscription [in]

Type: <b>const <a href="https://msdn.microsoft.com/723d2e27-420d-4eea-9ae1-d624807bf4ec">FWPM_FILTER_SUBSCRIPTION0</a>*</b>

The notifications to be delivered.


### -param callback [in]

Type: <b><a href="https://msdn.microsoft.com/6c0c41d7-ff84-4ae3-b9e0-ebc52cc6273d">FWPM_FILTER_CHANGE_CALLBACK0</a></b>

The  function pointer that will be invoked when a notification is ready for delivery.


### -param context [in, optional]

Type: <b>void*</b>

Optional context pointer. This pointer is passed to the <i>callback</i> function along with details of the change. 


### -param changeHandle [out]

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



Subscribers do not receive notifications for changes made with the same session handle used to subscribe. This is because subscribers only need  to see changes made by others since they already know which changes they made themselves.

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_SUBSCRIBE</a> access to the filter's container and 
   <b>FWPM_ACTRL_READ</b> access to the filter. The subscriber will only get notifications for filters to which it has
   <b>FWPM_ACTRL_READ</b> access. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmFilterSubscribeChanges0</b> is a specific implementation of FwpmFilterSubscribeChanges. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/6c0c41d7-ff84-4ae3-b9e0-ebc52cc6273d">FWPM_FILTER_CHANGE_CALLBACK0</a>



<a href="https://msdn.microsoft.com/723d2e27-420d-4eea-9ae1-d624807bf4ec">FWPM_FILTER_SUBSCRIPTION0</a>



<a href="https://msdn.microsoft.com/a7e78b38-9d24-4883-83a7-f4ecdf7ffb4c">FwpmFilterUnsubscribeChanges0</a>
 

 

