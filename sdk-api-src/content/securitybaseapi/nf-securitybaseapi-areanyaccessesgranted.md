---
UID: NF:securitybaseapi.AreAnyAccessesGranted
title: AreAnyAccessesGranted function (securitybaseapi.h)
description: Tests whether any of a set of requested access rights has been granted. The access rights are represented as bit flags in an access mask.
helpviewer_keywords: ["AreAnyAccessesGranted","AreAnyAccessesGranted function [Security]","_win32_areanyaccessesgranted","security.areanyaccessesgranted","securitybaseapi/AreAnyAccessesGranted"]
old-location: security\areanyaccessesgranted.htm
tech.root: security
ms.assetid: 4bac6ebc-716a-4725-b9e6-a109b27dfc18
ms.date: 12/05/2018
ms.keywords: AreAnyAccessesGranted, AreAnyAccessesGranted function [Security], _win32_areanyaccessesgranted, security.areanyaccessesgranted, securitybaseapi/AreAnyAccessesGranted
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
 - AreAnyAccessesGranted
 - securitybaseapi/AreAnyAccessesGranted
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
 - AreAnyAccessesGranted
---

# AreAnyAccessesGranted function


## -description

The <b>AreAnyAccessesGranted</b> function tests whether any of a set of requested access rights has been granted. The access rights are represented as bit flags in an <a href="/windows/desktop/SecGloss/a-gly">access mask</a>.

## -parameters

### -param GrantedAccess [in]

Specifies the granted access mask.

### -param DesiredAccess [in]

Specifies the access mask to be requested. This mask must have been mapped from generic to specific and standard access rights, usually by calling the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a> function.

## -returns

If any of the requested access rights have been granted, the return value is nonzero.

If none of the requested access rights have been granted, the return value is zero.

## -remarks

The <b>AreAnyAccessesGranted</b> function is often used by a server application to check the access rights of a client attempting to gain access to an object. When any of the bits set in the <i>DesiredAccess</i> parameter match the bits set in the <i>GrantedAccess</i> parameter, at least one of the requested access rights has been granted.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted">AreAllAccessesGranted</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>