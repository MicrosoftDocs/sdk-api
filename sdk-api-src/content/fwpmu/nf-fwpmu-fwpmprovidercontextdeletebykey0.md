---
UID: NF:fwpmu.FwpmProviderContextDeleteByKey0
title: FwpmProviderContextDeleteByKey0 function
author: windows-sdk-content
description: Removes a provider context from the system.
old-location: fwp\fwpmprovidercontextdeletebykey0_func.htm
old-project: fwp
ms.assetid: 453ab1f7-d137-4252-9445-7195624a5465
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FwpmProviderContextDeleteByKey0, FwpmProviderContextDeleteByKey0 function [Filtering], fwp.fwpmprovidercontextdeletebykey0_func, fwpmu/FwpmProviderContextDeleteByKey0
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
 - FwpmProviderContextDeleteByKey0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmProviderContextDeleteByKey0 function


## -description



		The <b>FwpmProviderContextDeleteByKey0</b> function removes a provider context from the system.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of the object being removed from the system. This is a pointer to the same GUID that was specified when the application called <a href="https://msdn.microsoft.com/c31595b8-81e4-4399-b2a3-d228c35875fe">FwpmProviderContextAdd0</a> for this object.


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
The provider context was successfully deleted.

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

The caller needs <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">DELETE</a> access to the provider context. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>FwpmProviderContextDeleteByKey0</b> is a specific implementation of FwpmProviderContextDeleteByKey. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/c31595b8-81e4-4399-b2a3-d228c35875fe">FwpmProviderContextAdd0</a>
 

 

