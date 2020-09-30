---
UID: NF:fwpmu.FwpmvSwitchEventsGetSecurityInfo0
title: FwpmvSwitchEventsGetSecurityInfo0 function (fwpmu.h)
description: Retrieves a copy of the security descriptor for a vSwitch event.
helpviewer_keywords: ["FwpmvSwitchEventsGetSecurityInfo0","FwpmvSwitchEventsGetSecurityInfo0 function [Filtering]","fwp.fwpmvswitcheventsgetsecurityinfo0","fwpmu/FwpmvSwitchEventsGetSecurityInfo0"]
old-location: fwp\fwpmvswitcheventsgetsecurityinfo0.htm
tech.root: fwp
ms.assetid: 20183a71-f750-4131-8d29-80a0624f8b8d
ms.date: 12/05/2018
ms.keywords: FwpmvSwitchEventsGetSecurityInfo0, FwpmvSwitchEventsGetSecurityInfo0 function [Filtering], fwp.fwpmvswitcheventsgetsecurityinfo0, fwpmu/FwpmvSwitchEventsGetSecurityInfo0
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FwpmvSwitchEventsGetSecurityInfo0
 - fwpmu/FwpmvSwitchEventsGetSecurityInfo0
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
 - FwpmvSwitchEventsGetSecurityInfo0
---

# FwpmvSwitchEventsGetSecurityInfo0 function


## -description

The <b>FwpmvSwitchEventsGetSecurityInfo0</b> function retrieves a copy of the security descriptor for a vSwitch event.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param securityInfo [in]

Type: <b><a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a></b>

The type of security information to retrieve.

### -param sidOwner [out]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-sid">PSID</a>*</b>

The owner security identifier (SID) in the returned security descriptor.

### -param sidGroup [out]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-sid">PSID</a>*</b>

The primary group security identifier (SID) in the returned security descriptor.

### -param dacl [out]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-acl">PACL</a>*</b>

The discretionary access control list (DACL) in the returned security descriptor.

### -param sacl [out]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-acl">PACL</a>*</b>

The system access control list (SACL) in the returned security descriptor.

### -param securityDescriptor [out]

Type: <b><a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">PSECURITY_DESCRIPTOR</a>*</b>

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

The returned <i>securityDescriptor</i> parameter must be freed through a call to <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmfreememory0">FwpmFreeMemory0</a>. The other four returned parameters must not be freed, as they point to addresses within the <i>securityDescriptor</i> parameter.

This function behaves like the standard Win32 	<a href="/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo">GetSecurityInfo</a> function. The caller needs the same standard access rights as described in the <b>GetSecurityInfo</b> reference topic.

<b>FwpmvSwitchEventsGetSecurityInfo0</b> is a specific implementation of FwpmvSwitchEventsGetSecurityInfo. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

<a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0">FwpmvSwitchEventsSetSecurityInfo0</a>



<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>