---
UID: NF:ntsecapi.LsaConnectUntrusted
title: LsaConnectUntrusted function (ntsecapi.h)
author: windows-sdk-content
description: Establishes an untrusted connection to the LSA server.
old-location: security\lsaconnectuntrusted.htm
tech.root: SecAuthN
ms.assetid: b54917c8-51cd-4891-9613-f37a4a46448b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LsaConnectUntrusted, LsaConnectUntrusted function [Security], _lsa_lsaconnectuntrusted, ntsecapi/LsaConnectUntrusted, security.lsaconnectuntrusted
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
 - LsaConnectUntrusted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LsaConnectUntrusted function


## -description


The <b>LsaConnectUntrusted</b> function establishes an untrusted connection to the LSA server.


## -parameters




### -param LsaHandle [out]

Pointer to a handle that receives the connection handle, which must be provided in future authentication services.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -remarks



<b>LsaConnectUntrusted</b> returns a handle to an untrusted connection; it does not verify any information about the caller. The handle should be closed using the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaderegisterlogonprocess">LsaDeregisterLogonProcess</a> function.

If your application simply needs to query information from authentication packages, you can use the handle returned by this function in calls to 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupauthenticationpackage">LsaLookupAuthenticationPackage</a>.

Applications with the SeTcbPrivilege privilege may create a trusted connection by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaregisterlogonprocess">LsaRegisterLogonProcess</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaderegisterlogonprocess">LsaDeregisterLogonProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupauthenticationpackage">LsaLookupAuthenticationPackage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaregisterlogonprocess">LsaRegisterLogonProcess</a>
 

 

