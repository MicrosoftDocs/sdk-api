---
UID: NF:fwpmu.FwpmConnectionSetSecurityInfo0
title: FwpmConnectionSetSecurityInfo0 function (fwpmu.h)
description: Sets specified security information in the security descriptor for a connection object change event.helpviewer_keywords: ["FwpmConnectionSetSecurityInfo0","FwpmConnectionSetSecurityInfo0 function [Filtering]","fwp.fwpmconnectionsetsecurityinfo0","fwpmu/FwpmConnectionSetSecurityInfo0"]
old-location: fwp\fwpmconnectionsetsecurityinfo0.htm
tech.root: fwp
ms.assetid: 74c976b0-68a5-4e09-8c6f-6ccb2766e0ad
ms.date: 12/05/2018
ms.keywords: FwpmConnectionSetSecurityInfo0, FwpmConnectionSetSecurityInfo0 function [Filtering], fwp.fwpmconnectionsetsecurityinfo0, fwpmu/FwpmConnectionSetSecurityInfo0
f1_keywords:
- fwpmu/FwpmConnectionSetSecurityInfo0
dev_langs:
- c++
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
- FwpmConnectionSetSecurityInfo0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FwpmConnectionSetSecurityInfo0 function


## -description


The <b>FwpmConnectionSetSecurityInfo0</b> function sets specified security information in the security  descriptor for a connection object change event.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle to an open session to the filter engine. Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param securityInfo [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a></b>

The type of security information to set.


### -param sidOwner [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a>*</b>

The owner's security identifier (SID) to be set in the security descriptor.


### -param sidGroup [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a>*</b>

The group's SID to be set in the security descriptor.


### -param dacl [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>*</b>

The discretionary access control list (DACL) to be set in the security descriptor.


### -param sacl [in, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>*</b>

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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0">FwpmConnectionGetSecurityInfo0</a>
 

 

