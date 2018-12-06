---
UID: NF:fwpmu.FwpmFilterDeleteByKey0
title: FwpmFilterDeleteByKey0 function
author: windows-sdk-content
description: Removes a filter object from the system.
old-location: fwp\fwpmfilterdeletebykey0_func.htm
tech.root: fwp
ms.assetid: 75c0796c-84d0-4282-bc93-267a17dd3edc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FwpmFilterDeleteByKey0, FwpmFilterDeleteByKey0 function [Filtering], fwp.fwpmfilterdeletebykey0_func, fwpmu/FwpmFilterDeleteByKey0
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
 - FwpmFilterDeleteByKey0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmFilterDeleteByKey0 function


## -description


The <b>FwpmFilterDeleteByKey0</b> function removes a filter object from the system.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of the object being removed from the system. This is the same GUID that was specified when the application called <a href="https://msdn.microsoft.com/ca11187e-3a91-438f-9a7f-606da7c88f6d">FwpmFilterAdd0</a> for this object.


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
The filter was successfully deleted.

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



This function cannot be called from within a read-only transaction. It will fail with
<b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

This function can be called within a dynamic session if the corresponding object was added during the same session. If this function is called for an object that was added during a different dynamic session, it will fail with <b>FWP_E_WRONG_SESSION</b>. If this function is called for an object that was not added during a dynamic session, it will fail with <b>FWP_E_DYNAMIC_SESSION_IN_PROGRESS</b>.

The caller needs <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">DELETE</a> access to the filter. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmFilterDeleteByKey0</b> is a specific implementation of FwpmFilterDeleteByKey. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/ca11187e-3a91-438f-9a7f-606da7c88f6d">FwpmFilterAdd0</a>



<a href="https://msdn.microsoft.com/5ab0942c-aee2-44f9-9e7f-568405131691">FwpmFilterGetByKey0</a>
 

 

