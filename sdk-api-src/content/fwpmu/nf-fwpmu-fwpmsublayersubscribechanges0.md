---
UID: NF:fwpmu.FwpmSubLayerSubscribeChanges0
title: FwpmSubLayerSubscribeChanges0 function (fwpmu.h)
author: windows-sdk-content
description: Is used to request the delivery of notifications regarding changes in a particular sublayer.
old-location: fwp\fwpmsublayersubscribechanges0_func.htm
tech.root: fwp
ms.assetid: 63b672ab-6625-417a-86ff-7b834d7444cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FwpmSubLayerSubscribeChanges0, FwpmSubLayerSubscribeChanges0 function [Filtering], fwp.fwpmsublayersubscribechanges0_func, fwpmu/FwpmSubLayerSubscribeChanges0
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
 - FwpmSubLayerSubscribeChanges0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmSubLayerSubscribeChanges0 function


## -description


The <b>FwpmSubLayerSubscribeChanges0</b> function  is used to request the delivery of notifications regarding changes in a particular sublayer.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param subscription [in]

Type: <b>const <a href="https://msdn.microsoft.com/bfd0f35a-7f56-42e4-b3da-cd7c4a2bae5e">FWPM_SUBLAYER_SUBSCRIPTION0</a>*</b>

The notifications to be delivered.


### -param callback [in]

Type: <b><a href="https://msdn.microsoft.com/b608d13f-bc76-478b-b18f-527f438a1222">FWPM_SUBLAYER_CHANGE_CALLBACK0</a></b>

Function pointer that will be invoked when a notification is ready for delivery.


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

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_SUBSCRIBE</a> access to the sublayer's container and 
   <b>FWPM_ACTRL_READ</b> access to the sub-layer. The subscriber will only get notifications for sublayers to which it has
   <b>FWPM_ACTRL_READ</b> access. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmSubLayerSubscribeChanges0</b> is a specific implementation of FwpmSubLayerSubscribeChanges. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/b608d13f-bc76-478b-b18f-527f438a1222">FWPM_SUBLAYER_CHANGE_CALLBACK0</a>



<a href="https://msdn.microsoft.com/bfd0f35a-7f56-42e4-b3da-cd7c4a2bae5e">FWPM_SUBLAYER_SUBSCRIPTION0</a>
 

 

