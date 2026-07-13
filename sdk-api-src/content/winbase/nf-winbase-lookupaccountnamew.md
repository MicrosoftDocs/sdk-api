---
UID: NF:winbase.LookupAccountNameW
title: LookupAccountNameW function (winbase.h)
description: Accepts the name of a system and an account as input. It retrieves a security identifier (SID) for the account and the name of the domain on which the account was found. (Unicode)
helpviewer_keywords: ["LookupAccountName", "LookupAccountName function [Security]", "LookupAccountNameW", "_win32_lookupaccountname", "security.lookupaccountname", "winbase/LookupAccountName", "winbase/LookupAccountNameW"]
old-location: security\lookupaccountname.htm
tech.root: security
ms.assetid: 72855539-469a-4289-99cc-eae2ed89901f
ms.date: 12/05/2018
ms.keywords: LookupAccountName, LookupAccountName function [Security], LookupAccountNameA, LookupAccountNameW, _win32_lookupaccountname, security.lookupaccountname, winbase/LookupAccountName, winbase/LookupAccountNameA, winbase/LookupAccountNameW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupAccountNameW (Unicode) and LookupAccountNameA (ANSI)
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
 - LookupAccountNameW
 - winbase/LookupAccountNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-security-lsalookup-l2-1-0.dll
 - API-MS-Win-security-lsalookup-l2-1-1.dll
 - API-MS-Win-Security-LSALookup-L2-1-2.dll
 - API-MS-Win-Security-LSALookup-Ansi-L2-1-0.dll
api_name:
 - LookupAccountName
 - LookupAccountNameA
 - LookupAccountNameW
---

# LookupAccountNameW function


## -description

The <b>LookupAccountName</b> function accepts the name of a system and an account as input. It retrieves a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) for the account and the name of the domain on which the account was found.

The <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames">LsaLookupNames</a> function can also retrieve computer accounts.

## -parameters

### -param lpSystemName [in, optional]

A pointer to a <b>null</b>-terminated character string that specifies the name of the system. This string can be the name of a remote computer. If this string is <b>NULL</b>, the account name translation begins on the local system. If the name cannot be resolved on the local system, this function will try to resolve the name using domain controllers trusted by the local system. Generally, specify a value for  <i>lpSystemName</i> only when the  account is in an untrusted domain and the   name of a computer in that domain is known.

### -param lpAccountName [in]

A pointer to a <b>null</b>-terminated string that specifies the account name.

Use a fully qualified string in the domain_name\user_name format to ensure that <b>LookupAccountName</b> finds the account in the desired domain.

### -param Sid [out, optional]

A pointer to a buffer that receives the 
<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that corresponds to the account name pointed to by the <i>lpAccountName</i> parameter. If this parameter is <b>NULL</b>, <i>cbSid</i> must be zero.

### -param cbSid [in, out]

A pointer to a variable. On input, this value specifies the size, in bytes, of the <i>Sid</i> buffer. If the function fails because the buffer is too small or if <i>cbSid</i> is zero, this variable receives the required buffer size.

### -param ReferencedDomainName [out, optional]

A pointer to a buffer that receives the name of the domain where the account name is found. For computers that are not joined to a domain, this buffer receives the computer name. If this parameter is <b>NULL</b>, <i>cchReferencedDomainName</i> must be zero.

### -param cchReferencedDomainName [in, out]

A pointer to a variable. On input, this value specifies the size, in <b>TCHAR</b>s, of the <i>ReferencedDomainName</i> buffer. If the function fails because the buffer is too small, this variable receives the required buffer size, including the terminating <b>null</b> character.

### -param peUse [out]

A pointer to a 
<a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a> enumerated type that indicates the type of the account when the function returns.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>LookupAccountName</b> function attempts to find a SID for the specified name by first checking a list of well-known SIDs. If the name does not correspond to a well-known SID, the function checks built-in and administratively defined local accounts. Next, the function checks the primary domain. If the name is not found there, trusted domains are checked.

Use fully qualified account names (for example, domain_name\user_name) instead of isolated names (for example, user_name). Fully qualified names are unambiguous and provide better performance when the lookup is performed. This function also supports fully qualified DNS names (for example, example.example.com\user_name) and <a href="/windows/desktop/SecGloss/u-gly">user principal names</a> (UPN) (for example, someone@example.com).

In addition to looking up local accounts, local domain accounts, and explicitly trusted domain accounts, <b>LookupAccountName</b> can look up the name for any account in any domain in the forest.





> [!NOTE]
> The winbase.h header defines LookupAccountName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-equalprefixsid">EqualPrefixSid</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getusernamea">GetUserName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountsida">LookupAccountSid</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames2">LsaLookupNames2</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a>
