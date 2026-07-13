---
UID: NF:securitybaseapi.CheckTokenMembershipEx
title: CheckTokenMembershipEx function (securitybaseapi.h)
description: Determines whether the specified SID is enabled in the specified token.
helpviewer_keywords: ["CheckTokenMembershipEx","CheckTokenMembershipEx function [Security]","security.checktokenmembershipex","securitybaseapi/CheckTokenMembershipEx"]
old-location: security\checktokenmembershipex.htm
tech.root: security
ms.assetid: 0420FC77-8035-42A5-8907-83D0CE53FB64
ms.date: 12/05/2018
ms.keywords: CheckTokenMembershipEx, CheckTokenMembershipEx function [Security], security.checktokenmembershipex, securitybaseapi/CheckTokenMembershipEx
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CheckTokenMembershipEx
 - securitybaseapi/CheckTokenMembershipEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Kernel32.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - CheckTokenMembershipEx
---

# CheckTokenMembershipEx function


## -description

The <b>CheckTokenMembershipEx</b> function determines whether the specified SID is enabled in the specified token.

## -parameters

### -param TokenHandle [in, optional]

A handle to an access token. If present, this token is checked for the SID. If not present, then the current effective token is used. This must be an impersonation token.

### -param SidToCheck [in]

A pointer to a SID structure. The function checks for the presence of this SID in the presence of the token.

### -param Flags [in]

Flags that affect the behavior of the function. Currently the only valid flag is CTMF_INCLUDE_APPCONTAINER which allows app containers to pass the call as long as the other requirements of the token are met, such as the group specified is present and enabled.

### -param IsMember [out]

<b>TRUE</b> if the SID is enabled in the token; otherwise, <b>FALSE</b>.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.