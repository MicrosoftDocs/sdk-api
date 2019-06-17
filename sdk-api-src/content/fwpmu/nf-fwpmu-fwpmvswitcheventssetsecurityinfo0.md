---
UID: NF:fwpmu.FwpmvSwitchEventsSetSecurityInfo0
title: FwpmvSwitchEventsSetSecurityInfo0 function (fwpmu.h)
author: windows-sdk-content
description: Sets specified security information in the security descriptor for a vSwitch event.
old-location: fwp\fwpmvswitcheventssetsecurityinfo0.htm
tech.root: fwp
ms.assetid: 2e20986a-9ebf-493b-8d32-ac9b709747ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FwpmvSwitchEventsSetSecurityInfo0, FwpmvSwitchEventsSetSecurityInfo0 function [Filtering], fwp.fwpmvswitcheventssetsecurityinfo0, fwpmu/FwpmvSwitchEventsSetSecurityInfo0
ms.topic: function
f1_keywords: ["fwpmu/FwpmvSwitchEventsSetSecurityInfo0"]
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
 - FwpmvSwitchEventsSetSecurityInfo0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FwpmvSwitchEventsSetSecurityInfo0 function


## -description


The <b>FwpmvSwitchEventsSetSecurityInfo0</b> function sets specified security information in the security  descriptor for a vSwitch event.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle to an open session to the filter engine. Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param securityInfo [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a></b>

The type of security information to set.


### -param sidOwner [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid">SID</a>*</b>

The owner's security identifier (SID) to be set in the security descriptor.


### -param sidGroup [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_sid">SID</a>*</b>

The group's SID to be set in the security descriptor.


### -param dacl [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_acl">ACL</a>*</b>

The discretionary access control list (DACL) to be set in the security descriptor.


### -param sacl [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_acl">ACL</a>*</b>

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
A Windows Filtering Platform (WFP) specific error. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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



This function cannot be called from within a transaction. It will fail with
<b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://docs.microsoft.com/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

This function cannot be called from within a dynamic session. It will fail with
<b>FWP_E_DYNAMIC_SESSION_IN_PROGRESS</b>. See <a href="https://docs.microsoft.com/windows/desktop/FWP/object-management">Object Management</a> for more information about sessions.

This function behaves like the standard Win32 	 <a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a> function. The caller needs the same standard access rights as described in the <b>SetSecurityInfo</b> reference topic.

<b>FwpmvSwitchEventsSetSecurityInfo0</b> is a specific implementation of FwpmvSwitchEventsSetSecurityInfo. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0">FwpmvSwitchEventsGetSecurityInfo0</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-functions">WFP  Functions</a>
 

 

