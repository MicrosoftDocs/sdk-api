---
UID: NF:fwpmu.FwpmFilterSetSecurityInfoByKey0
title: FwpmFilterSetSecurityInfoByKey0 function
author: windows-sdk-content
description: Sets specified security information in the security descriptor of a filter object.
old-location: fwp\fwpmfiltersetsecurityinfobykey0_func.htm
tech.root: fwp
ms.assetid: 01dac90a-98a0-46b7-8d9e-ce5fdf8014a9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FwpmFilterSetSecurityInfoByKey0, FwpmFilterSetSecurityInfoByKey0 function [Filtering], fwp.fwpmfiltersetsecurityinfobykey0_func, fwpmu/FwpmFilterSetSecurityInfoByKey0
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
 - FwpmFilterSetSecurityInfoByKey0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmFilterSetSecurityInfoByKey0 function


## -description


The <b>FwpmFilterSetSecurityInfoByKey0</b> function sets specified security information in the security descriptor of a filter object.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param key [in, optional]

Type: <b>const GUID*</b>

Unique identifier of the filter. This GUID was specified in the <b>filterKey</b> member of the <i>filter</i> parameter when the application called <a href="https://msdn.microsoft.com/ca11187e-3a91-438f-9a7f-606da7c88f6d">FwpmFilterAdd0</a> for this object.


### -param securityInfo [in]

Type: <b><a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a></b>

The type of security information to set.


### -param sidOwner [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>*</b>

The owner's security identifier (SID) to be set in the security descriptor.


### -param sidGroup [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>*</b>

The group's SID to be set in the security descriptor.


### -param dacl [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>*</b>

The discretionary access control list (DACL) to be set in the security descriptor.


### -param sacl [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>*</b>

The system access control list (SACL) to be set in the security descriptor.


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
The security descriptor was set successfully.

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



If the <i>key</i> parameter is <b>NULL</b> or if it is  a <b>NULL</b> GUID, this function manages the security information of the filters container.

This function cannot be called from within a transaction. It will fail with
<b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

This function can be called within a dynamic session if the corresponding object was added during the same session. If this function is called for an object that was added during a different dynamic session, it will fail with <b>FWP_E_WRONG_SESSION</b>. If this function is called for an object that was not added during a dynamic session, it will fail with <b>FWP_E_DYNAMIC_SESSION_IN_PROGRESS</b>.

This function behaves like the standard Win32 	 <a href="https://msdn.microsoft.com/f1781ba9-81eb-46f9-b530-c390b67d65de">SetSecurityInfo</a> function. The caller needs the same standard access rights as described in the <b>SetSecurityInfo</b> reference topic.

<b>FwpmFilterSetSecurityInfoByKey0</b> is a specific implementation of FwpmFilterSetSecurityInfoByKey. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/9d35f4ca-b268-45de-b252-527b3a6fbd93">FwpmFilterGetSecurityInfoByKey0</a>
 

 

