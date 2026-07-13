---
UID: NF:securitybaseapi.DestroyPrivateObjectSecurity
title: DestroyPrivateObjectSecurity function (securitybaseapi.h)
description: Deletes a private object's security descriptor.
helpviewer_keywords: ["DestroyPrivateObjectSecurity","DestroyPrivateObjectSecurity function [Security]","_win32_destroyprivateobjectsecurity","security.destroyprivateobjectsecurity","securitybaseapi/DestroyPrivateObjectSecurity"]
old-location: security\destroyprivateobjectsecurity.htm
tech.root: security
ms.assetid: 4ef10852-8229-41de-a4d7-d2845e4c92ce
ms.date: 12/05/2018
ms.keywords: DestroyPrivateObjectSecurity, DestroyPrivateObjectSecurity function [Security], _win32_destroyprivateobjectsecurity, security.destroyprivateobjectsecurity, securitybaseapi/DestroyPrivateObjectSecurity
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
 - DestroyPrivateObjectSecurity
 - securitybaseapi/DestroyPrivateObjectSecurity
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
 - DestroyPrivateObjectSecurity
---

# DestroyPrivateObjectSecurity function


## -description

The <b>DestroyPrivateObjectSecurity</b> function deletes a private object's <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>. For background information, see the <a href="/windows/desktop/SecAuthZ/security-descriptors-for-private-objects">Security Descriptors for Private Objects</a> topic.

## -parameters

### -param ObjectDescriptor [in, out]

A pointer to a pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure to be deleted. This security descriptor must have been created by a call to the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity">CreatePrivateObjectSecurity</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity">CreatePrivateObjectSecurity</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity">GetPrivateObjectSecurity</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/SecAuthZ/security-descriptors-for-private-objects">Security Descriptors for Private Objects</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity">SetPrivateObjectSecurity</a>