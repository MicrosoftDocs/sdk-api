---
UID: NF:securitybaseapi.FreeSid
title: FreeSid function (securitybaseapi.h)
description: Frees a security identifier (SID) previously allocated by using the AllocateAndInitializeSid function.
helpviewer_keywords: ["FreeSid","FreeSid function [Security]","_win32_freesid","security.freesid","securitybaseapi/FreeSid"]
old-location: security\freesid.htm
tech.root: security
ms.assetid: 1e2098d8-4d1f-4353-97c1-549021a5b3fd
ms.date: 12/05/2018
ms.keywords: FreeSid, FreeSid function [Security], _win32_freesid, security.freesid, securitybaseapi/FreeSid
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
 - FreeSid
 - securitybaseapi/FreeSid
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
 - FreeSid
---

# FreeSid function


## -description

The <b>FreeSid</b> function frees a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) previously allocated by using the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a> function.

## -parameters

### -param pSid [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure to free.

## -returns

If the function succeeds, the function returns <b>NULL</b>.

If the function fails, it returns a pointer to the <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure represented by the <i>pSid</i> parameter.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>