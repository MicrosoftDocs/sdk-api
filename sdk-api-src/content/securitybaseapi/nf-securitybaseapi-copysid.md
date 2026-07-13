---
UID: NF:securitybaseapi.CopySid
title: CopySid function (securitybaseapi.h)
description: Copies a security identifier (SID) to a buffer.
helpviewer_keywords: ["CopySid","CopySid function [Security]","_win32_copysid","security.copysid","securitybaseapi/CopySid"]
old-location: security\copysid.htm
tech.root: security
ms.assetid: 2d7c182e-cdf8-4604-97bf-468bb4bd9232
ms.date: 12/05/2018
ms.keywords: CopySid, CopySid function [Security], _win32_copysid, security.copysid, securitybaseapi/CopySid
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
 - CopySid
 - securitybaseapi/CopySid
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
 - CopySid
---

# CopySid function


## -description

The <b>CopySid</b> function copies a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) to a buffer.

## -parameters

### -param nDestinationSidLength [in]

Specifies the length, in bytes, of the buffer receiving the copy of the SID.

### -param pDestinationSid [out]

A pointer to a buffer that receives a copy of the source 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure.

### -param pSourceSid [in]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that the function copies to the buffer pointed to by the <i>pDestinationSid</i> parameter.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application can use the <b>CopySid</b> function to make a copy of a SID in an <a href="/windows/desktop/SecGloss/a-gly">access token</a> (for example, in a <a href="/windows/desktop/api/winnt/ns-winnt-token_groups">TOKEN_GROUPS</a> structure) to use in an access control entry (<a href="/windows/desktop/SecGloss/a-gly">ACE</a>).


#### Examples

For an example that uses this function, see <a href="/previous-versions/aa446670(v=vs.85)">Getting the Logon SID</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-equalsid">EqualSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getlengthsid">GetLengthSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired">GetSidLengthRequired</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesid">InitializeSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>