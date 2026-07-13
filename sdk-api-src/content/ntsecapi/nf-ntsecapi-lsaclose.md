---
UID: NF:ntsecapi.LsaClose
title: LsaClose function (ntsecapi.h)
description: The LsaClose function closes a handle to a Policy or TrustedDomain object.
helpviewer_keywords: ["LsaClose","LsaClose function [Security]","_lsa_lsaclose","ntsecapi/LsaClose","security.lsaclose"]
old-location: security\lsaclose.htm
tech.root: security
ms.assetid: 6283b1da-4ec3-48e1-91f6-321c6390befe
ms.date: 12/05/2018
ms.keywords: LsaClose, LsaClose function [Security], _lsa_lsaclose, ntsecapi/LsaClose, security.lsaclose
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LsaClose
 - ntsecapi/LsaClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-lsapolicy-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaClose
---

# LsaClose function


## -description

The <b>LsaClose</b> function closes a handle to a Policy or <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object.

## -parameters

### -param ObjectHandle [in]

A handle to a <a href="/windows/desktop/SecMgmt/policy-object">Policy</a> object returned by the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy">LsaOpenPolicy</a> function or to a <a href="/windows/desktop/SecMgmt/trusteddomain-object">TrustedDomain</a> object returned by the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname">LsaOpenTrustedDomainByName</a> function. Following the completion of this call, the handle is no longer valid.

## -returns

If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="/windows/desktop/SecMgmt/management-return-values">LSA Policy Function Return Values</a>.

You can use the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsantstatustowinerror">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy">LsaOpenPolicy</a>