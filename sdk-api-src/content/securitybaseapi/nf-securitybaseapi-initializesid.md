---
UID: NF:securitybaseapi.InitializeSid
title: InitializeSid function (securitybaseapi.h)
description: Initializes a security identifier (SID).
helpviewer_keywords: ["InitializeSid","InitializeSid function [Security]","_win32_initializesid","security.initializesid","securitybaseapi/InitializeSid"]
old-location: security\initializesid.htm
tech.root: security
ms.assetid: b2d803a5-faaf-4066-ba2c-0442c71bb150
ms.date: 12/05/2018
ms.keywords: InitializeSid, InitializeSid function [Security], _win32_initializesid, security.initializesid, securitybaseapi/InitializeSid
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
 - InitializeSid
 - securitybaseapi/InitializeSid
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
 - InitializeSid
---

# InitializeSid function


## -description

The <b>InitializeSid</b> function initializes a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

## -parameters

### -param Sid [out]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure to be initialized.

### -param pIdentifierAuthority [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a> structure to set in the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure.

### -param nSubAuthorityCount [in]

Specifies the number of subauthorities to set in the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>. Values of the subauthority must be set separately, as described in the following Remarks section.

## -returns

If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Although the <b>InitializeSid</b> function sets the number of subauthorities for the SID, it does not set the subauthority values. This must be done separately, using functions such as <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>.

An application can use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a> function to initialize a SID and set its subauthority values.

This function uses a 32-bit RID value. For applications that require a larger RID value, use 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getlengthsid">GetLengthSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired">GetSidLengthRequired</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount">GetSidSubAuthorityCount</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a>