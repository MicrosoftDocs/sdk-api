---
UID: NF:ntsecapi.LsaRegisterLogonProcess
title: LsaRegisterLogonProcess function
author: windows-sdk-content
description: Establishes a connection to the LSA server and verifies that the caller is a logon application.
old-location: security\lsaregisterlogonprocess.htm
tech.root: secauthn
ms.assetid: 1bef2949-b4c8-400e-8a2d-60aa88a4e238
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: LsaRegisterLogonProcess, LsaRegisterLogonProcess function [Security], _lsa_lsaregisterlogonprocess, ntsecapi/LsaRegisterLogonProcess, security.lsaregisterlogonprocess
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - LsaRegisterLogonProcess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsaRegisterLogonProcess function


## -description


The <b>LsaRegisterLogonProcess</b> function establishes a connection to the LSA server and verifies that the caller is a logon application.


## -parameters




### -param LogonProcessName [in]

Pointer to an 
<a href="https://msdn.microsoft.com/4ae4160f-bcad-41d9-8239-91da44702b76">LSA_STRING</a> structure identifying the logon application. This should be a printable name suitable for display to administrators. For example, the Windows logon application might use the name "User32LogonProcess". This name is used by the LSA during auditing. <b>LsaRegisterLogonProcess</b> does not check whether the name is already in use. 




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
<a href="https://msdn.microsoft.com/66b78404-02c2-48e9-92c3-d27b68f77c23">LsaAddAccountRights</a>.

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
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -remarks



This function must be called before a logon process may use any other logon authentication functions provided by the LSA.

The <b>LsaRegisterLogonProcess</b> function verifies that the application making the function call is a logon process by checking that it has the SeTcbPrivilege privilege set. It also opens the application's process for PROCESS_DUP_HANDLE access in anticipation of future LSA authentication calls. For more information, see 
<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>.

When you have finished using the connection to the LSA server, delete the caller's logon application context and close the connection by calling the <a href="https://msdn.microsoft.com/8a956469-9538-4d71-8158-af22aa26f840">LsaDeregisterLogonProcess</a> function.




## -see-also




<a href="https://msdn.microsoft.com/66b78404-02c2-48e9-92c3-d27b68f77c23">LsaAddAccountRights</a>



<a href="https://msdn.microsoft.com/b54917c8-51cd-4891-9613-f37a4a46448b">LsaConnectUntrusted</a>



<a href="https://msdn.microsoft.com/8a956469-9538-4d71-8158-af22aa26f840">LsaDeregisterLogonProcess</a>
 

 

