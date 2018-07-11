---
UID: NF:fwpmu.FwpmvSwitchEventsGetSecurityInfo0
title: FwpmvSwitchEventsGetSecurityInfo0 function
author: windows-sdk-content
description: Retrieves a copy of the security descriptor for a vSwitch event.
old-location: fwp\fwpmvswitcheventsgetsecurityinfo0.htm
old-project: fwp
ms.assetid: 20183a71-f750-4131-8d29-80a0624f8b8d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: FwpmvSwitchEventsGetSecurityInfo0, FwpmvSwitchEventsGetSecurityInfo0 function [Filtering], fwp.fwpmvswitcheventsgetsecurityinfo0, fwpmu/FwpmvSwitchEventsGetSecurityInfo0
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
 - FwpmvSwitchEventsGetSecurityInfo0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# FwpmvSwitchEventsGetSecurityInfo0 function


## -description


The <b>FwpmvSwitchEventsGetSecurityInfo0</b> function retrieves a copy of the security descriptor for a vSwitch event.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param securityInfo [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a></b>

The type of security information to retrieve.


### -param sidOwner [out]

Type: <b><a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">PSID</a>*</b>

The owner security identifier (SID) in the returned security descriptor.


### -param sidGroup [out]

Type: <b><a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">PSID</a>*</b>

The primary group security identifier (SID) in the returned security descriptor.


### -param dacl [out]

Type: <b><a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">PACL</a>*</b>

The discretionary access control list (DACL) in the returned security descriptor.


### -param sacl [out]

Type: <b><a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">PACL</a>*</b>

The system access control list (SACL) in the returned security descriptor.


### -param securityDescriptor [out]

Type: <b><a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">PSECURITY_DESCRIPTOR</a>*</b>

The returned security descriptor.


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
The security descriptor was successfully retrieved.

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



The returned <i>securityDescriptor</i> parameter must be freed through a call to <a href="https://msdn.microsoft.com/ba9f8c1e-f75c-4bf0-b68b-e21a358575fc">FwpmFreeMemory0</a>. The other four returned parameters must not be freed, as they point to addresses within the <i>securityDescriptor</i> parameter.

This function behaves like the standard Win32 	<a href="https://msdn.microsoft.com/64767a6b-cd79-4e02-881a-706a078ff446">GetSecurityInfo</a> function. The caller needs the same standard access rights as described in the <b>GetSecurityInfo</b> reference topic.

<b>FwpmvSwitchEventsGetSecurityInfo0</b> is a specific implementation of FwpmvSwitchEventsGetSecurityInfo. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/2e20986a-9ebf-493b-8d32-ac9b709747ac">FwpmvSwitchEventsSetSecurityInfo0</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

