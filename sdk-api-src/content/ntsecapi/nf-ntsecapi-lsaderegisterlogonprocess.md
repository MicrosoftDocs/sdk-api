---
UID: NF:ntsecapi.LsaDeregisterLogonProcess
title: LsaDeregisterLogonProcess function (ntsecapi.h)
description: Deletes the caller's logon application context and closes the connection to the LSA server.
helpviewer_keywords: ["LsaDeregisterLogonProcess","LsaDeregisterLogonProcess function [Security]","_lsa_lsaderegisterlogonprocess","ntsecapi/LsaDeregisterLogonProcess","security.lsaderegisterlogonprocess"]
old-location: security\lsaderegisterlogonprocess.htm
tech.root: security
ms.assetid: 8a956469-9538-4d71-8158-af22aa26f840
ms.date: 12/05/2018
ms.keywords: LsaDeregisterLogonProcess, LsaDeregisterLogonProcess function [Security], _lsa_lsaderegisterlogonprocess, ntsecapi/LsaDeregisterLogonProcess, security.lsaderegisterlogonprocess
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
 - LsaDeregisterLogonProcess
 - ntsecapi/LsaDeregisterLogonProcess
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
 - LsaDeregisterLogonProcess
---

# LsaDeregisterLogonProcess function


## -description

The <b>LsaDeregisterLogonProcess</b> function deletes the caller's logon application context and closes the connection to the LSA server.

## -parameters

### -param LsaHandle [in]

Handle obtained from a 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaregisterlogonprocess">LsaRegisterLogonProcess</a> or 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaconnectuntrusted">LsaConnectUntrusted</a> call.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -remarks

If your logon application references the connection handle after calling the <b>LsaDeregisterLogonProcess</b> function, unexpected behavior can result.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaconnectuntrusted">LsaConnectUntrusted</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaregisterlogonprocess">LsaRegisterLogonProcess</a>