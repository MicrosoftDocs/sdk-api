---
UID: NF:securitybaseapi.GetSidIdentifierAuthority
title: GetSidIdentifierAuthority function (securitybaseapi.h)
description: Returns a pointer to the SID_IDENTIFIER_AUTHORITY structure in a specified security identifier (SID).
helpviewer_keywords: ["GetSidIdentifierAuthority","GetSidIdentifierAuthority function [Security]","_win32_getsididentifierauthority","security.getsididentifierauthority","securitybaseapi/GetSidIdentifierAuthority"]
old-location: security\getsididentifierauthority.htm
tech.root: security
ms.assetid: 67a06e7b-775f-424c-ab36-0fc9b93b801a
ms.date: 12/05/2018
ms.keywords: GetSidIdentifierAuthority, GetSidIdentifierAuthority function [Security], _win32_getsididentifierauthority, security.getsididentifierauthority, securitybaseapi/GetSidIdentifierAuthority
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
 - GetSidIdentifierAuthority
 - securitybaseapi/GetSidIdentifierAuthority
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
 - GetSidIdentifierAuthority
---

# GetSidIdentifierAuthority function


## -description

The <b>GetSidIdentifierAuthority</b> function returns a pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a> structure in a specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

## -parameters

### -param pSid [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure for which a pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a> structure is returned.

This function does not handle <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structures that are not valid. Call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a> function to verify that the <b>SID</b> structure is valid before you call this function.

## -returns

If the function succeeds, the return value is a pointer to the <a href="/windows/desktop/api/winnt/ns-winnt-sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a> structure for the specified 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure.

If the function fails, the return value is undefined. The function fails if the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure pointed to by the <i>pSid</i> parameter is not valid. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function uses a 32-bit RID value. For applications that require a larger RID value, use 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a> and related functions.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getlengthsid">GetLengthSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired">GetSidLengthRequired</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a>