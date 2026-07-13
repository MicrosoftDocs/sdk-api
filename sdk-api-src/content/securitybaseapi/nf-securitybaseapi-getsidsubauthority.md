---
UID: NF:securitybaseapi.GetSidSubAuthority
title: GetSidSubAuthority function (securitybaseapi.h)
description: Returns a pointer to a specified subauthority in a security identifier (SID). The subauthority value is a relative identifier (RID).
helpviewer_keywords: ["GetSidSubAuthority","GetSidSubAuthority function [Security]","_win32_getsidsubauthority","security.getsidsubauthority","securitybaseapi/GetSidSubAuthority"]
old-location: security\getsidsubauthority.htm
tech.root: security
ms.assetid: 3a2d07f3-f1da-477d-b93f-525e3459dc61
ms.date: 12/05/2018
ms.keywords: GetSidSubAuthority, GetSidSubAuthority function [Security], _win32_getsidsubauthority, security.getsidsubauthority, securitybaseapi/GetSidSubAuthority
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
 - GetSidSubAuthority
 - securitybaseapi/GetSidSubAuthority
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
 - GetSidSubAuthority
---

# GetSidSubAuthority function


## -description

The <b>GetSidSubAuthority</b> function returns a pointer to a specified subauthority in a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID). The subauthority value is a <a href="/windows/desktop/SecGloss/r-gly">relative identifier</a> (RID).

## -parameters

### -param pSid [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure from which a pointer to a subauthority is to be returned.

This function does not handle <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structures that are not valid. Call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a> function to verify that the <b>SID</b> structure is valid before you call this function.

### -param nSubAuthority [in]

Specifies an index value identifying the subauthority array element whose address the function will return. The function performs no validation tests on this value. An application can call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a> function to discover the range of acceptable values.

## -returns

If the function succeeds, the return value is a pointer to the specified <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> subauthority. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the function fails, the return value is undefined. The function fails if the specified <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure is not valid or if the index value specified by the <i>nSubAuthority</i> parameter is out of bounds.

## -remarks

The <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure specified in <i>pSid</i> uses a 32-bit RID value. For applications that require longer RID values, use 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a> and related functions.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getlengthsid">GetLengthSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired">GetSidLengthRequired</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>