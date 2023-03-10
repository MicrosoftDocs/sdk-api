---
UID: NF:fwpmu.IPsecKeyManagerSetSecurityInfoByKey0
title: IPsecKeyManagerSetSecurityInfoByKey0 function (fwpmu.h)
description: Sets specified security information in the security descriptor that controls access to the key manager.
helpviewer_keywords: ["IPsecKeyManagerSetSecurityInfoByKey0","IPsecKeyManagerSetSecurityInfoByKey0 function [Filtering]","fwp.ipseckeymanagersetsecurityinfobykey0","fwpmu/IPsecKeyManagerSetSecurityInfoByKey0"]
old-location: fwp\ipseckeymanagersetsecurityinfobykey0.htm
tech.root: fwp
ms.assetid: 15C8BB3B-0345-42A6-8C99-4D92FC0AEDE4
ms.date: 12/05/2018
ms.keywords: IPsecKeyManagerSetSecurityInfoByKey0, IPsecKeyManagerSetSecurityInfoByKey0 function [Filtering], fwp.ipseckeymanagersetsecurityinfobykey0, fwpmu/IPsecKeyManagerSetSecurityInfoByKey0
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
 - IPsecKeyManagerSetSecurityInfoByKey0
 - fwpmu/IPsecKeyManagerSetSecurityInfoByKey0
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
 - IPsecKeyManagerSetSecurityInfoByKey0
---

# IPsecKeyManagerSetSecurityInfoByKey0 function


## -description

The <b>IPsecKeyManagerSetSecurityInfoByKey0</b> function sets specified security information in the security descriptor that controls access to the key manager.

## -parameters

### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle to an open session to the filter engine. Call <a href="/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.

### -param reserved

Type: <b>const void*</b>

Reserved. Should be specified as NULL.

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

## -see-also

<a href="/windows/desktop/FWP/fwp-functions">WFP  Functions</a>