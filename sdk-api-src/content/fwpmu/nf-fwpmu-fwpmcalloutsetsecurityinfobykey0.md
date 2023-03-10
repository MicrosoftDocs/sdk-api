---
UID: NF:fwpmu.FwpmCalloutSetSecurityInfoByKey0
title: FwpmCalloutSetSecurityInfoByKey0 function (fwpmu.h)
description: Sets specified security information in the security descriptor of a callout object.
helpviewer_keywords: ["FwpmCalloutSetSecurityInfoByKey0","FwpmCalloutSetSecurityInfoByKey0 function [Filtering]","fwp.fwpmcalloutsetsecurityinfobykey0_func","fwpmu/FwpmCalloutSetSecurityInfoByKey0"]
old-location: fwp\fwpmcalloutsetsecurityinfobykey0_func.htm
tech.root: fwp
ms.assetid: c85b3eb1-29c8-47f1-9d68-8e65e06b5492
ms.date: 12/05/2018
ms.keywords: FwpmCalloutSetSecurityInfoByKey0, FwpmCalloutSetSecurityInfoByKey0 function [Filtering], fwp.fwpmcalloutsetsecurityinfobykey0_func, fwpmu/FwpmCalloutSetSecurityInfoByKey0
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
 - FwpmCalloutSetSecurityInfoByKey0
 - fwpmu/FwpmCalloutSetSecurityInfoByKey0
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
 - FwpmCalloutSetSecurityInfoByKey0
---

# FwpmCalloutSetSecurityInfoByKey0 function


## -description

The <b>FwpmCalloutSetSecurityInfoByKey0</b> function sets specified security information in the security descriptor of a callout object.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param key [in, optional]

Type: <b>const GUID*</b>

Pointer to a GUID that uniquely identifies the callout. This GUID was specified in the <b>calloutKey</b> member of the <i>callout</i> parameter when the application called <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmcalloutadd0">FwpmCalloutAdd0</a> for this object.

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

If the <i>key</i> parameter is <b>NULL</b> or if it is  a <b>NULL</b> GUID, this function manages the security information of the callouts container.

This function cannot be called from within a transaction. It will fail with
<b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="/windows/desktop/FWP/object-management">Object Management</a> for more information about transactions.

This function can be called within a dynamic session if the corresponding object was added during the same session. If this function is called for an object that was added during a different dynamic session, it will fail with <b>FWP_E_WRONG_SESSION</b>. If this function is called for an object that was not added during a dynamic session, it will fail with <b>FWP_E_DYNAMIC_SESSION_IN_PROGRESS</b>.

This function behaves like the standard Win32 	 <a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a> function. The caller needs the same standard access rights as described in the <b>SetSecurityInfo</b> reference topic.

<b>FwpmCalloutSetSecurityInfoByKey0</b> is a specific implementation of FwpmCalloutSetSecurityInfoByKey. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmcalloutgetsecurityinfobykey0">FwpmCalloutGetSecurityInfoByKey0</a>