---
UID: NF:ntsecapi.LsaDeregisterLogonProcess
title: LsaDeregisterLogonProcess function
author: windows-sdk-content
description: Deletes the caller's logon application context and closes the connection to the LSA server.
old-location: security\lsaderegisterlogonprocess.htm
old-project: secauthn
ms.assetid: 8a956469-9538-4d71-8158-af22aa26f840
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LsaDeregisterLogonProcess, LsaDeregisterLogonProcess function [Security], _lsa_lsaderegisterlogonprocess, ntsecapi/LsaDeregisterLogonProcess, security.lsaderegisterlogonprocess
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - LsaDeregisterLogonProcess
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
req.product: ADAM
---

# LsaDeregisterLogonProcess function


## -description


The <b>LsaDeregisterLogonProcess</b> function deletes the caller's logon application context and closes the connection to the LSA server.


## -parameters




### -param LsaHandle [in]

Handle obtained from a 
<a href="https://msdn.microsoft.com/1bef2949-b4c8-400e-8a2d-60aa88a4e238">LsaRegisterLogonProcess</a> or 
<a href="https://msdn.microsoft.com/b54917c8-51cd-4891-9613-f37a4a46448b">LsaConnectUntrusted</a> call.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -remarks



If your logon application references the connection handle after calling the <b>LsaDeregisterLogonProcess</b> function, unexpected behavior can result.




## -see-also




<a href="https://msdn.microsoft.com/b54917c8-51cd-4891-9613-f37a4a46448b">LsaConnectUntrusted</a>



<a href="https://msdn.microsoft.com/1bef2949-b4c8-400e-8a2d-60aa88a4e238">LsaRegisterLogonProcess</a>
 

 

