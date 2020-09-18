---
UID: NF:ntsecapi.LsaFreeReturnBuffer
title: LsaFreeReturnBuffer function (ntsecapi.h)
description: Frees the memory used by a buffer previously allocated by the LSA.
helpviewer_keywords: ["LsaFreeReturnBuffer","LsaFreeReturnBuffer function [Security]","_lsa_lsafreereturnbuffer","ntsecapi/LsaFreeReturnBuffer","security.lsafreereturnbuffer"]
old-location: security\lsafreereturnbuffer.htm
tech.root: security
ms.assetid: e814ed68-07e7-4936-ba96-5411086f43f6
ms.date: 12/05/2018
ms.keywords: LsaFreeReturnBuffer, LsaFreeReturnBuffer function [Security], _lsa_lsafreereturnbuffer, ntsecapi/LsaFreeReturnBuffer, security.lsafreereturnbuffer
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
 - LsaFreeReturnBuffer
 - ntsecapi/LsaFreeReturnBuffer
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
 - LsaFreeReturnBuffer
---

# LsaFreeReturnBuffer function


## -description

The <b>LsaFreeReturnBuffer</b> function frees the memory used by a buffer previously allocated by the LSA.

## -parameters

### -param Buffer [in]

Pointer to the buffer to be freed.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.

## -remarks

Some of the LSA authentication functions allocate memory buffers to hold returned information, for example, 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> and 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>. Your application should call <b>LsaFreeReturnBuffer</b> to free these buffers when they are no longer needed.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a>