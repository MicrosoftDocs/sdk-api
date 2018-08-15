---
UID: NF:fwpmu.IPsecKeyManagerSetSecurityInfoByKey0
title: IPsecKeyManagerSetSecurityInfoByKey0 function
author: windows-sdk-content
description: Sets specified security information in the security descriptor that controls access to the key manager.
old-location: fwp\ipseckeymanagersetsecurityinfobykey0.htm
old-project: fwp
ms.assetid: 15C8BB3B-0345-42A6-8C99-4D92FC0AEDE4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPsecKeyManagerSetSecurityInfoByKey0, IPsecKeyManagerSetSecurityInfoByKey0 function [Filtering], fwp.ipseckeymanagersetsecurityinfobykey0, fwpmu/IPsecKeyManagerSetSecurityInfoByKey0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.redist: 
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
 - IPsecKeyManagerSetSecurityInfoByKey0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# IPsecKeyManagerSetSecurityInfoByKey0 function


## -description


The <b>IPsecKeyManagerSetSecurityInfoByKey0</b> function sets specified security information in the security descriptor that controls access to the key manager.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle to an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param reserved

Type: <b>const void*</b>

Reserved. Should be specified as NULL.


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
The security information was successfully set.

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
 




## -see-also




<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

