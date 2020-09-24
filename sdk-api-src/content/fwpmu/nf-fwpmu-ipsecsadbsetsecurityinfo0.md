---
UID: NF:fwpmu.IPsecSaDbSetSecurityInfo0
title: IPsecSaDbSetSecurityInfo0 function (fwpmu.h)
description: Sets specified security information in the security descriptor of the IPsec security association database.
helpviewer_keywords: ["IPsecSaDbSetSecurityInfo0","IPsecSaDbSetSecurityInfo0 function [Filtering]","fwp.ipsecsadbsetsecurityinfo0","fwpmu/IPsecSaDbSetSecurityInfo0"]
old-location: fwp\ipsecsadbsetsecurityinfo0.htm
tech.root: fwp
ms.assetid: 6e51c04f-c829-4452-9e40-2c97551ad0f0
ms.date: 12/05/2018
ms.keywords: IPsecSaDbSetSecurityInfo0, IPsecSaDbSetSecurityInfo0 function [Filtering], fwp.ipsecsadbsetsecurityinfo0, fwpmu/IPsecSaDbSetSecurityInfo0
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
 - IPsecSaDbSetSecurityInfo0
 - fwpmu/IPsecSaDbSetSecurityInfo0
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
 - IPsecSaDbSetSecurityInfo0
---

# IPsecSaDbSetSecurityInfo0 function


## -description

The <b>IPsecSaDbSetSecurityInfo0</b> function sets specified security information in the security descriptor of the IPsec security association database.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

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

This function behaves like the standard Win32 	 <a href="/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo">SetSecurityInfo</a> function. The caller needs the same standard access rights as described in the <b>SetSecurityInfo</b> reference topic.

<b>IPsecSaDbSetSecurityInfo0</b> is a specific implementation of IPsecSaDbSetSecurityInfo. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-ipsecsadbgetsecurityinfo0">IPsecSaDbGetSecurityInfo0</a>