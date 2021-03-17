---
UID: NF:ntsecapi.LsaConnectUntrusted
title: LsaConnectUntrusted function (ntsecapi.h)
description: Establishes an untrusted connection to the LSA server.
helpviewer_keywords: ["LsaConnectUntrusted","LsaConnectUntrusted function [Security]","_lsa_lsaconnectuntrusted","ntsecapi/LsaConnectUntrusted","security.lsaconnectuntrusted"]
old-location: security\lsaconnectuntrusted.htm
tech.root: security
ms.assetid: b54917c8-51cd-4891-9613-f37a4a46448b
ms.date: 12/05/2018
ms.keywords: LsaConnectUntrusted, LsaConnectUntrusted function [Security], _lsa_lsaconnectuntrusted, ntsecapi/LsaConnectUntrusted, security.lsaconnectuntrusted
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
 - LsaConnectUntrusted
 - ntsecapi/LsaConnectUntrusted
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
 - LsaConnectUntrusted
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
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -remarks

<b>LsaConnectUntrusted</b> returns a handle to an untrusted connection; it does not verify any information about the caller. The handle should be closed using the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaderegisterlogonprocess">LsaDeregisterLogonProcess</a> function.

If your application simply needs to query information from authentication packages, you can use the handle returned by this function in calls to 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupauthenticationpackage">LsaLookupAuthenticationPackage</a>.

Applications with the SeTcbPrivilege privilege may create a trusted connection by calling 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaregisterlogonprocess">LsaRegisterLogonProcess</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaderegisterlogonprocess">LsaDeregisterLogonProcess</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupauthenticationpackage">LsaLookupAuthenticationPackage</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaregisterlogonprocess">LsaRegisterLogonProcess</a>