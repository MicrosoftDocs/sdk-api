---
UID: NF:fwpmu.IPsecSaDbSetSecurityInfo0
title: IPsecSaDbSetSecurityInfo0 function
author: windows-sdk-content
description: Sets specified security information in the security descriptor of the IPsec security association database.
old-location: fwp\ipsecsadbsetsecurityinfo0.htm
old-project: fwp
ms.assetid: 6e51c04f-c829-4452-9e40-2c97551ad0f0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPsecSaDbSetSecurityInfo0, IPsecSaDbSetSecurityInfo0 function [Filtering], fwp.ipsecsadbsetsecurityinfo0, fwpmu/IPsecSaDbSetSecurityInfo0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.redist: 
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
 - IPsecSaDbSetSecurityInfo0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# IPsecSaDbSetSecurityInfo0 function


## -description


The <b>IPsecSaDbSetSecurityInfo0</b> function sets specified security information in the security descriptor of the IPsec security association database.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


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
The security information was set successfully.

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



This function behaves like the standard Win32 	 <a href="https://msdn.microsoft.com/f1781ba9-81eb-46f9-b530-c390b67d65de">SetSecurityInfo</a> function. The caller needs the same standard access rights as described in the <b>SetSecurityInfo</b> reference topic.

<b>IPsecSaDbSetSecurityInfo0</b> is a specific implementation of IPsecSaDbSetSecurityInfo. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/19121de3-91bc-4dca-94f8-599a43bb1e68">IPsecSaDbGetSecurityInfo0</a>
 

 

