---
UID: NF:securitybaseapi.IsValidSid
title: IsValidSid function (securitybaseapi.h)
description: Validates a security identifier (SID) by verifying that the revision number is within a known range, and that the number of subauthorities is less than the maximum.
helpviewer_keywords: ["IsValidSid","IsValidSid function [Security]","_win32_isvalidsid","security.isvalidsid","securitybaseapi/IsValidSid"]
old-location: security\isvalidsid.htm
tech.root: security
ms.assetid: 0fb08512-90a1-4a5c-9b4c-121bf7701bba
ms.date: 12/05/2018
ms.keywords: IsValidSid, IsValidSid function [Security], _win32_isvalidsid, security.isvalidsid, securitybaseapi/IsValidSid
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
 - IsValidSid
 - securitybaseapi/IsValidSid
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
 - IsValidSid
---

# IsValidSid function


## -description

The <b>IsValidSid</b> function validates a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) by verifying that the revision number is within a known range, and that the number of subauthorities is less than the maximum.

## -parameters

### -param pSid [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure to validate. This parameter cannot be <b>NULL</b>.

## -returns

If the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure is valid, the return value is nonzero.

If the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure is not valid, the return value is zero. There is no extended error information for this function; do not call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <i>pSid</i> is <b>NULL</b>, the application will fail with an access violation.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getlengthsid">GetLengthSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired">GetSidLengthRequired</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>