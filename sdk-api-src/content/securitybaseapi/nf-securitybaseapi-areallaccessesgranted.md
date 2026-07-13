---
UID: NF:securitybaseapi.AreAllAccessesGranted
title: AreAllAccessesGranted function (securitybaseapi.h)
description: Checks whether a set of requested access rights has been granted. The access rights are represented as bit flags in an access mask.
helpviewer_keywords: ["AreAllAccessesGranted","AreAllAccessesGranted function [Security]","_win32_areallaccessesgranted","security.areallaccessesgranted","securitybaseapi/AreAllAccessesGranted"]
old-location: security\areallaccessesgranted.htm
tech.root: security
ms.assetid: 91349693-8667-49dd-a813-657497b7d467
ms.date: 12/05/2018
ms.keywords: AreAllAccessesGranted, AreAllAccessesGranted function [Security], _win32_areallaccessesgranted, security.areallaccessesgranted, securitybaseapi/AreAllAccessesGranted
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
 - AreAllAccessesGranted
 - securitybaseapi/AreAllAccessesGranted
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
 - AreAllAccessesGranted
---

# AreAllAccessesGranted function


## -description

The <b>AreAllAccessesGranted</b> function checks whether a set of requested access rights has been granted. The access rights are represented as bit flags in an <a href="/windows/desktop/SecGloss/a-gly">access mask</a>.

## -parameters

### -param GrantedAccess [in]

An access mask that specifies the access rights that have been granted.

### -param DesiredAccess [in]

An access mask that specifies the access rights that have been requested. This mask must have been mapped from generic to specific and standard access rights, usually by calling the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a> function.

## -returns

If all requested access rights have been granted, the return value is nonzero.

If not all requested access rights have been granted, the return value is zero.

## -remarks

The <b>AreAllAccessesGranted</b> function is commonly used by a server application to check the access rights of a client attempting to gain access to an object. When the bits set in the <i>DesiredAccess</i> parameter match the bits set in the <i>GrantedAccess</i> parameter, all requested rights have been granted.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted">AreAnyAccessesGranted</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-mapgenericmask">MapGenericMask</a>