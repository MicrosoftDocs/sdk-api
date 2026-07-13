---
UID: NF:securitybaseapi.GetSidLengthRequired
title: GetSidLengthRequired function (securitybaseapi.h)
description: Returns the length, in bytes, of the buffer required to store a SID with a specified number of subauthorities.
helpviewer_keywords: ["GetSidLengthRequired","GetSidLengthRequired function [Security]","_win32_getsidlengthrequired","security.getsidlengthrequired","securitybaseapi/GetSidLengthRequired"]
old-location: security\getsidlengthrequired.htm
tech.root: security
ms.assetid: a481fb4f-20bd-4f44-a3d5-d8b8d6228339
ms.date: 12/05/2018
ms.keywords: GetSidLengthRequired, GetSidLengthRequired function [Security], _win32_getsidlengthrequired, security.getsidlengthrequired, securitybaseapi/GetSidLengthRequired
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetSidLengthRequired
 - securitybaseapi/GetSidLengthRequired
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - GetSidLengthRequired
---

# GetSidLengthRequired function


## -description

The <b>GetSidLengthRequired</b> function returns the length, in bytes, of the buffer required to store a SID with a specified number of subauthorities.

## -parameters

### -param nSubAuthorityCount [in]

Specifies the number of subauthorities to be stored in the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure.

## -returns

The return value is the length, in bytes, of the buffer required to store the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure. This function cannot fail.

## -remarks

The <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure specified in <i>nSubAuthorityCount</i> uses a 32-bit RID value. For applications that require longer RID values, use 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a> and related functions.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getlengthsid">GetLengthSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesid">InitializeSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>