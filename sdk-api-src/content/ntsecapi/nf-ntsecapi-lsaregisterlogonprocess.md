---
UID: NF:ntsecapi.LsaRegisterLogonProcess
title: LsaRegisterLogonProcess function (ntsecapi.h)
description: Establishes a connection to the LSA server and verifies that the caller is a logon application.
helpviewer_keywords: ["LsaRegisterLogonProcess","LsaRegisterLogonProcess function [Security]","_lsa_lsaregisterlogonprocess","ntsecapi/LsaRegisterLogonProcess","security.lsaregisterlogonprocess"]
old-location: security\lsaregisterlogonprocess.htm
tech.root: security
ms.assetid: 1bef2949-b4c8-400e-8a2d-60aa88a4e238
ms.date: 12/05/2018
ms.keywords: LsaRegisterLogonProcess, LsaRegisterLogonProcess function [Security], _lsa_lsaregisterlogonprocess, ntsecapi/LsaRegisterLogonProcess, security.lsaregisterlogonprocess
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaRegisterLogonProcess
 - ntsecapi/LsaRegisterLogonProcess
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - LsaRegisterLogonProcess
---

# LsaRegisterLogonProcess function


## -description

The <b>LsaRegisterLogonProcess</b> function establishes a connection to the LSA server and verifies that the caller is a logon application.

## -parameters

### -param LogonProcessName [in]

Pointer to an 
<a href="/windows/desktop/api/lsalookup/ns-lsalookup-lsa_string">LSA_STRING</a> structure identifying the logon application. This should be a printable name suitable for display to administrators. For example, the Windows logon application might use the name "User32LogonProcess". This name is used by the LSA during auditing. <b>LsaRegisterLogonProcess</b> does not check whether the name is already in use. 




This string must not exceed 127 bytes.

### -param LsaHandle [out]

Pointer that receives a handle used in future authentication function calls.

### -param SecurityMode [out]

The value returned is not meaningful and should be ignored.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. The following are possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_PORT_CONNECTION_REFUSED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have the SeTcbPrivilege privilege, which is required to call this function. 




You can set this privilege by calling 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights">LsaAddAccountRights</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NAME_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The specified logon process name exceeds 127 bytes.

</td>
</tr>
</table>
 

For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -remarks

This function must be called before a logon process may use any other logon authentication functions provided by the LSA.

The <b>LsaRegisterLogonProcess</b> function verifies that the application making the function call is a logon process by checking that it has the SeTcbPrivilege privilege set. It also opens the application's process for PROCESS_DUP_HANDLE access in anticipation of future LSA authentication calls. For more information, see 
<a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>.

When you have finished using the connection to the LSA server, delete the caller's logon application context and close the connection by calling the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaderegisterlogonprocess">LsaDeregisterLogonProcess</a> function.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights">LsaAddAccountRights</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaconnectuntrusted">LsaConnectUntrusted</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaderegisterlogonprocess">LsaDeregisterLogonProcess</a>