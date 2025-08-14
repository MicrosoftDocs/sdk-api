---
UID: NF:securitybaseapi.EqualDomainSid
title: EqualDomainSid function (securitybaseapi.h)
description: Determines whether two SIDs are from the same domain.
helpviewer_keywords: ["EqualDomainSid","EqualDomainSid function [Security]","_win32_equaldomainsid","security.equaldomainsid","securitybaseapi/EqualDomainSid"]
old-location: security\equaldomainsid.htm
tech.root: security
ms.assetid: a7eea3bd-33e0-427c-b023-07851c192eb2
ms.date: 12/05/2018
ms.keywords: EqualDomainSid, EqualDomainSid function [Security], _win32_equaldomainsid, security.equaldomainsid, securitybaseapi/EqualDomainSid
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
 - EqualDomainSid
 - securitybaseapi/EqualDomainSid
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
 - EqualDomainSid
---

# EqualDomainSid function


## -description

The <b>EqualDomainSid</b> function determines whether two SIDs are from the same domain.

## -parameters

### -param pSid1 [in]

A pointer to one of the two SIDs to compare. This SID must be either an account domain SID or a BUILTIN SID.

### -param pSid2 [in]

A pointer to one of the two SIDs to compare. This SID must be either an account domain SID or a BUILTIN SID.

### -param pfEqual [out]

A pointer to a BOOL that <b>EqualDomainSid</b> sets to <b>TRUE</b> if the domains of the two SIDs are equal or <b>FALSE</b> if they are not equal. This value cannot be <b>NULL</b>.

## -returns

If both SIDs are  account domain SIDs and/or BUILTIN SIDs, the return value is nonzero. In addition, *<i>pfEqual</i> is set to <b>TRUE</b> if the domains of the two SIDs are equal; otherwise  *<i>pfEqual</i> is set to <b>FALSE</b>.

If one or more of the SIDS is neither an account domain SID nor a BUILTIN SID, then the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>GetLastError</b> returns ERROR_NON_DOMAIN_SID if either SID is not an account domain SID or BUILTIN SID.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-equalprefixsid">EqualPrefixSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-equalsid">EqualSid</a>