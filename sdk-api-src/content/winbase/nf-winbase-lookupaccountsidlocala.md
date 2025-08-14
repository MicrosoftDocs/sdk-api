---
UID: NF:winbase.LookupAccountSidLocalA
title: LookupAccountSidLocalA macro (winbase.h)
description: Retrieves the name of the account for the specified SID on the local machine. (ANSI)
helpviewer_keywords: ["LookupAccountSidLocalA", "winbase/LookupAccountSidLocalA"]
old-location: security\lookupaccountsidlocal.htm
tech.root: security
ms.assetid: B039FFD7-B483-4CC0-B606-FAA5003DA238
ms.date: 11/28/2022
ms.keywords: LookupAccountSidLocal, LookupAccountSidLocal function [Security], LookupAccountSidLocalA, LookupAccountSidLocalW, security.lookupaccountsidlocal, winbase/LookupAccountSidLocal, winbase/LookupAccountSidLocalA, winbase/LookupAccountSidLocalW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupAccountSidLocalW (Unicode) and LookupAccountSidLocalA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LookupAccountSidLocalA
 - winbase/LookupAccountSidLocalA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-lsalookup-l1-1-2.dll
 - api-ms-win-security-lsalookup-l1-1-1.dll
 - sechost.dll
 - api-ms-win-security-lsalookup-l1-1-0.dll
api_name:
 - LookupAccountSidLocal
 - LookupAccountSidLocalA
 - LookupAccountSidLocalW
---

## -description

**LookupAccountSidLocalA** is defined as a macro that calls [LookupAccountSidA](nf-winbase-lookupaccountsida.md) with `NULL` as the first parameter. Retrieves the name of the account for the specified SID on the local machine.

## -parameters

### -param Sid [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> to look up.

### -param Name [out, optional]

A pointer to a buffer that receives a <b>null</b>-terminated string that contains the account name that corresponds to the <i>lpSid</i> parameter.

### -param cchName [in, out]

On input, specifies the size, in <b>TCHAR</b>s, of the <i>lpName</i> buffer. If the function fails because the buffer is too small or if <i>cchName</i> is zero, <i>cchName</i> receives the required buffer size, including the terminating <b>null</b> character.

### -param ReferencedDomainName [out, optional]

A pointer to a buffer that receives a <b>null</b>-terminated string that contains the name of the domain where the account name was found.

On a server, the domain name returned for most accounts in the security database of the local computer is the name of the domain for which the server is a domain controller.

On a workstation, the domain name returned for most accounts in the security database of the local computer is the name of the computer as of the last start of the system (backslashes are excluded). If the name of the computer changes, the old name continues to be returned as the domain name until the system is restarted.

Some accounts are predefined by the system. The domain name returned for these accounts is BUILTIN.

### -param cchReferencedDomainName [in, out]

On input, specifies the size, in <b>TCHAR</b>s, of the <i>lpReferencedDomainName</i> buffer. If the function fails because the buffer is too small or if <i>cchReferencedDomainName</i> is zero, <i>cchReferencedDomainName</i> receives the required buffer size, including the terminating <b>null</b> character.

### -param peUse [out]

A pointer to a variable that receives a 
<a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a> value that indicates the type of the account.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function is similar to <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountsida">LookupAccountSid</a>, but restricts the search to the local machine.

> [!NOTE]
> The winbase.h header defines LookupAccountSidLocal as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-equalprefixsid">EqualPrefixSid</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a>
