---
UID: NF:securitybaseapi.IsTokenRestricted
title: IsTokenRestricted function (securitybaseapi.h)
description: Indicates whether a token contains a list of restricted security identifiers (SIDs).
helpviewer_keywords: ["IsTokenRestricted","IsTokenRestricted function [Security]","_win32_istokenrestricted","security.istokenrestricted","securitybaseapi/IsTokenRestricted"]
old-location: security\istokenrestricted.htm
tech.root: security
ms.assetid: eaa63bb9-3084-4246-b2ab-f913bb7348fb
ms.date: 12/05/2018
ms.keywords: IsTokenRestricted, IsTokenRestricted function [Security], _win32_istokenrestricted, security.istokenrestricted, securitybaseapi/IsTokenRestricted
req.header: securitybaseapi.h
req.include-header: Windows.h
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
 - IsTokenRestricted
 - securitybaseapi/IsTokenRestricted
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
 - IsTokenRestricted
---

# IsTokenRestricted function


## -description

The <b>IsTokenRestricted</b> function indicates whether a token contains a list of restricted <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs).

## -parameters

### -param TokenHandle [in]

A handle to an <a href="/windows/desktop/SecGloss/a-gly">access token</a> to test.

## -returns

If the token contains a list of restricting SIDs, the return value is nonzero.

If the token does not contain a list of restricting SIDs, the return value is zero.

If an error occurs, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a> function can restrict a token by disabling SIDs, deleting privileges, and specifying a list of restricting SIDs. The <b>IsTokenRestricted</b> function checks only for the list of restricting SIDs. If a token does not have any restricting SIDs, <b>IsTokenRestricted</b> returns <b>FALSE</b>, even though the token was created by a call to <b>CreateRestrictedToken</b>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>