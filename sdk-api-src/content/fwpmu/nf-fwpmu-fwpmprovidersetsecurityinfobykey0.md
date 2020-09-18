---
UID: NF:fwpmu.FwpmProviderSetSecurityInfoByKey0
title: FwpmProviderSetSecurityInfoByKey0 function (fwpmu.h)
description: Sets specified security information in the security descriptor of a provider object.
helpviewer_keywords: ["FwpmProviderSetSecurityInfoByKey0","FwpmProviderSetSecurityInfoByKey0 function [Filtering]","fwp.fwpmprovidersetsecurityinfobykey0_func","fwpmu/FwpmProviderSetSecurityInfoByKey0"]
old-location: fwp\fwpmprovidersetsecurityinfobykey0_func.htm
tech.root: fwp
ms.assetid: 4451ae03-cdff-4b43-84cd-a80d639ba79f
ms.date: 12/05/2018
ms.keywords: FwpmProviderSetSecurityInfoByKey0, FwpmProviderSetSecurityInfoByKey0 function [Filtering], fwp.fwpmprovidersetsecurityinfobykey0_func, fwpmu/FwpmProviderSetSecurityInfoByKey0
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmProviderSetSecurityInfoByKey0
 - fwpmu/FwpmProviderSetSecurityInfoByKey0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmProviderSetSecurityInfoByKey0
---

# FwpmProviderSetSecurityInfoByKey0 function


## -description

The <b>FwpmProviderSetSecurityInfoByKey0</b> function sets specified security information in the security descriptor of a provider object.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param key [in, optional]

Type: <b>const GUID*</b>

 Unique identifier of the provider. This is the same GUID that was specified when the application called <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovideradd0">FwpmProviderAdd0</a> for this object.

### -param securityInfo [in]

Type: <b><a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a></b>

The type of security information to set.

### -param sidOwner [in, optional]

Type: <b>const <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>*</b>

The owner's security identifier (SID) to be set in the security descriptor.

### -param sidGroup [in, optional]

Type: <b>const <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>*</b>

The group's SID to be set in the security descriptor.

### -param dacl [in, optional]

Type: <b>const <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>*</b>

The discretionary access control list (DACL) to be set in the security descriptor.

### -param sacl [in, optional]

Type: <b>const <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>*</b>

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
A Windows Filtering Platform (WFP) specific error. See <a href="/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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

If the <i>key</i> parameter is <b>NULL</b> or if it is  a <b>NULL</b> GUID, this function manages the security information of the providers container.

This function cannot be called from within a transaction. It will fail with
<b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

This function can be called within a dynamic session if the corresponding object was added during the same session. If this function is called for an object that was added during a different dynamic session, it will fail with <b>FWP_E_WRONG_SESSION</b>. If this function is called for an object that was not added during a dynamic session, it will fail with <b>FWP_E_DYNAMIC_SESSION_IN_PROGRESS</b>.

This function behaves like the standard Win32 	 <a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a> function. The caller needs the same standard access rights as described in the <b>SetSecurityInfo</b> reference topic.

<b>FwpmProviderSetSecurityInfoByKey0</b> is a specific implementation of FwpmProviderSetSecurityInfoByKey. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidergetsecurityinfobykey0">FwpmProviderGetSecurityInfoByKey0</a>