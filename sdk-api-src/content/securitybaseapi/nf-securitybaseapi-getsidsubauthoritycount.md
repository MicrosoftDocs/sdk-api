---
UID: NF:securitybaseapi.GetSidSubAuthorityCount
title: GetSidSubAuthorityCount function (securitybaseapi.h)
description: Returns a pointer to the member in a security identifier (SID) structure that contains the subauthority count.
helpviewer_keywords: ["GetSidSubAuthorityCount","GetSidSubAuthorityCount function [Security]","_win32_getsidsubauthoritycount","security.getsidsubauthoritycount","securitybaseapi/GetSidSubAuthorityCount"]
old-location: security\getsidsubauthoritycount.htm
tech.root: security
ms.assetid: ca81fb91-f5a1-4dc6-83ec-eadb62a37805
ms.date: 12/05/2018
ms.keywords: GetSidSubAuthorityCount, GetSidSubAuthorityCount function [Security], _win32_getsidsubauthoritycount, security.getsidsubauthoritycount, securitybaseapi/GetSidSubAuthorityCount
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
 - GetSidSubAuthorityCount
 - securitybaseapi/GetSidSubAuthorityCount
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
 - GetSidSubAuthorityCount
---

# GetSidSubAuthorityCount function


## -description

The <b>GetSidSubAuthorityCount</b> function returns a pointer to the member in a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) structure that contains the subauthority count.

## -parameters

### -param pSid [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure from which a pointer to the subauthority count is returned.

This function does not handle <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structures that are not valid. Call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a> function to verify that the <b>SID</b> structure is valid before you call this function.

## -returns

If the function succeeds, the return value is a pointer to the subauthority count for the specified <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure.

If the function fails, the return value is undefined. The function fails if the specified <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure is not valid. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The SID structure specified in <i>pSid</i> uses a 32-bit value. For applications that require longer RID values, use 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a> and related functions.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getlengthsid">GetLengthSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired">GetSidLengthRequired</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>