---
UID: NF:securitybaseapi.EqualSid
title: EqualSid function (securitybaseapi.h)
description: Tests two security identifier (SID) values for equality. Two SIDs must match exactly to be considered equal.
helpviewer_keywords: ["EqualSid","EqualSid function [Security]","_win32_equalsid","security.equalsid","securitybaseapi/EqualSid"]
old-location: security\equalsid.htm
tech.root: security
ms.assetid: 08420df3-f6e6-462e-a2e6-d2a7a90be8ed
ms.date: 12/05/2018
ms.keywords: EqualSid, EqualSid function [Security], _win32_equalsid, security.equalsid, securitybaseapi/EqualSid
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
 - EqualSid
 - securitybaseapi/EqualSid
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
 - EqualSid
---

# EqualSid function


## -description

The <b>EqualSid</b> function tests two <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) values for equality. Two SIDs must match exactly to be considered equal.

## -parameters

### -param pSid1 [in]

A pointer to the first 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure to compare. This structure is assumed to be valid.

### -param pSid2 [in]

A pointer to the second <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure to compare. This structure is assumed to be valid.

## -returns

If the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structures are equal, the return value is nonzero.

If the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structures are not equal, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If either <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure is not valid, the return value is undefined.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-equalprefixsid">EqualPrefixSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidsid">IsValidSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>