---
UID: NF:securitybaseapi.AllocateLocallyUniqueId
title: AllocateLocallyUniqueId function (securitybaseapi.h)
description: Allocates a locally unique identifier (LUID).
helpviewer_keywords: ["AllocateLocallyUniqueId","AllocateLocallyUniqueId function [Security]","_win32_allocatelocallyuniqueid","security.allocatelocallyuniqueid","securitybaseapi/AllocateLocallyUniqueId"]
old-location: security\allocatelocallyuniqueid.htm
tech.root: security
ms.assetid: 5d730034-802b-4d37-bd28-68992779b93e
ms.date: 12/05/2018
ms.keywords: AllocateLocallyUniqueId, AllocateLocallyUniqueId function [Security], _win32_allocatelocallyuniqueid, security.allocatelocallyuniqueid, securitybaseapi/AllocateLocallyUniqueId
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
 - AllocateLocallyUniqueId
 - securitybaseapi/AllocateLocallyUniqueId
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
 - AllocateLocallyUniqueId
---

# AllocateLocallyUniqueId function


## -description

The <b>AllocateLocallyUniqueId</b> function allocates a locally unique identifier (<a href="/windows/desktop/SecGloss/l-gly">LUID</a>).

## -parameters

### -param Luid [out]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> structure that receives the allocated LUID.

## -returns

If the function succeeds, the return value is nonzero. 

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The allocated <a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> is unique to the local system only, and uniqueness is guaranteed only until the system is next restarted.

The allocated <a href="/windows/desktop/api/winnt/ns-winnt-luid">LUID</a> is guaranteed  to be nonzero if this function succeeds.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupprivilegevaluea">LookupPrivilegeValue</a>