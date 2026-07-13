---
UID: NF:securitybaseapi.AllocateAndInitializeSid
title: AllocateAndInitializeSid function (securitybaseapi.h)
description: Allocates and initializes a security identifier (SID) with up to eight subauthorities.
helpviewer_keywords: ["AllocateAndInitializeSid","AllocateAndInitializeSid function [Security]","_win32_allocateandinitializesid","security.allocateandinitializesid","securitybaseapi/AllocateAndInitializeSid"]
old-location: security\allocateandinitializesid.htm
tech.root: security
ms.assetid: fcdff2f8-7f43-4c0f-b548-4914b1991937
ms.date: 12/05/2018
ms.keywords: AllocateAndInitializeSid, AllocateAndInitializeSid function [Security], _win32_allocateandinitializesid, security.allocateandinitializesid, securitybaseapi/AllocateAndInitializeSid
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
 - AllocateAndInitializeSid
 - securitybaseapi/AllocateAndInitializeSid
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
 - AllocateAndInitializeSid
---

# AllocateAndInitializeSid function


## -description

The <b>AllocateAndInitializeSid</b> function allocates and initializes a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) with up to eight subauthorities.

## -parameters

### -param pIdentifierAuthority [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a> structure. This structure provides the top-level identifier authority value to set in the SID.

### -param nSubAuthorityCount [in]

Specifies the number of subauthorities to place in the SID. This parameter also identifies how many of the subauthority parameters have meaningful values. This parameter must contain a value from 1 to 8. 




For example, a value of 3 indicates that the subauthority values specified by the <i>dwSubAuthority0</i>, <i>dwSubAuthority1</i>, and <i>dwSubAuthority2</i> parameters have meaningful values and to ignore the remainder.

### -param nSubAuthority0 [in]

Subauthority value to place in the SID.

### -param nSubAuthority1 [in]

Subauthority value to place in the SID.

### -param nSubAuthority2 [in]

Subauthority value to place in the SID.

### -param nSubAuthority3 [in]

Subauthority value to place in the SID.

### -param nSubAuthority4 [in]

Subauthority value to place in the SID.

### -param nSubAuthority5 [in]

Subauthority value to place in the SID.

### -param nSubAuthority6 [in]

Subauthority value to place in the SID.

### -param nSubAuthority7 [in]

Subauthority value to place in the SID.

### -param pSid [out]

A pointer to a variable that receives the pointer to the allocated and initialized 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A SID allocated with the <b>AllocateAndInitializeSid</b> function must be freed by using the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-freesid">FreeSid</a> function.

This function creates a SID with a 32-bit RID value. For applications that require longer RID values, use 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createwellknownsid">CreateWellKnownSid</a>.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--">Creating a Security Descriptor for a New Object</a> or <a href="/windows/desktop/SecAuthZ/taking-object-ownership-in-c--">Taking Object Ownership</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-freesid">FreeSid</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority">GetSidIdentifierAuthority</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializesid">InitializeSid</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid_identifier_authority">SID_IDENTIFIER_AUTHORITY</a>



<a href="/windows/desktop/SecAuthZ/well-known-sids">Well-known SIDs</a>