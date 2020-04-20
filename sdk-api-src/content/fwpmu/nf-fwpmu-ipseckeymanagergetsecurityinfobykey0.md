---
UID: NF:fwpmu.IPsecKeyManagerGetSecurityInfoByKey0
title: IPsecKeyManagerGetSecurityInfoByKey0 function (fwpmu.h)
description: Retrieves a copy of the security descriptor that controls access to the key manager.helpviewer_keywords: ["IPsecKeyManagerGetSecurityInfoByKey0","IPsecKeyManagerGetSecurityInfoByKey0 function [Filtering]","fwp.ipseckeymanagergetsecurityinfobykey0","fwpmu/IPsecKeyManagerGetSecurityInfoByKey0"]
old-location: fwp\ipseckeymanagergetsecurityinfobykey0.htm
tech.root: fwp
ms.assetid: 38F5369F-7885-4EEF-AB21-C5A44E35FC5E
ms.date: 12/05/2018
ms.keywords: IPsecKeyManagerGetSecurityInfoByKey0, IPsecKeyManagerGetSecurityInfoByKey0 function [Filtering], fwp.ipseckeymanagergetsecurityinfobykey0, fwpmu/IPsecKeyManagerGetSecurityInfoByKey0
f1_keywords:
- fwpmu/IPsecKeyManagerGetSecurityInfoByKey0
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
- IPsecKeyManagerGetSecurityInfoByKey0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPsecKeyManagerGetSecurityInfoByKey0 function


## -description


The <b>IPsecKeyManagerGetSecurityInfoByKey0</b> function retrieves a copy of the security descriptor that controls access to the key manager.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle to an open session to the filter engine. Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-fwpmengineopen0">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param reserved

Type: <b>const void*</b>

Reserved. Must be set to NULL.


### -param securityInfo [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a></b>

The type of security information to retrieve.


### -param sidOwner [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">PSID</a>*</b>

The owner security identifier (SID) in the returned security descriptor.


### -param sidGroup [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">PSID</a>*</b>

The primary group security identifier (SID) in the returned security descriptor.


### -param dacl [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-acl">PACL</a>*</b>

The discretionary access control list (DACL) in the returned security descriptor.


### -param sacl [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-acl">PACL</a>*</b>

The system access control list (SACL) in the returned security descriptor.


### -param securityDescriptor [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-security_descriptor">PSECURITY_DESCRIPTOR</a>*</b>

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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-functions">WFP  Functions</a>
 

 

