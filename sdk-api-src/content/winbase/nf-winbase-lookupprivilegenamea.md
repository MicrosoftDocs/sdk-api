---
UID: NF:winbase.LookupPrivilegeNameA
title: LookupPrivilegeNameA function (winbase.h)
description: Retrieves the name that corresponds to the privilege represented on a specific system by a specified locally unique identifier (LUID). (ANSI)
helpviewer_keywords: ["LookupPrivilegeNameA", "winbase/LookupPrivilegeNameA"]
old-location: security\lookupprivilegename.htm
tech.root: security
ms.assetid: 580fb58f-1470-4389-9f07-8f37403e2bdf
ms.date: 12/05/2018
ms.keywords: LookupPrivilegeName, LookupPrivilegeName function [Security], LookupPrivilegeNameA, LookupPrivilegeNameW, _win32_lookupprivilegename, security.lookupprivilegename, winbase/LookupPrivilegeName, winbase/LookupPrivilegeNameA, winbase/LookupPrivilegeNameW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupPrivilegeNameW (Unicode) and LookupPrivilegeNameA (ANSI)
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
 - LookupPrivilegeNameA
 - winbase/LookupPrivilegeNameA
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
 - LookupPrivilegeName
 - LookupPrivilegeNameA
 - LookupPrivilegeNameW
---

# LookupPrivilegeNameA function


## -description

The <b>LookupPrivilegeName</b> function retrieves the name that corresponds to the privilege represented on a specific system by a specified <a href="/windows/desktop/SecGloss/l-gly">locally unique identifier</a> (LUID).

## -parameters

### -param lpSystemName [in, optional]

A pointer to a null-terminated string that specifies the name of the system on which the privilege name is retrieved. If a null string is specified, the function attempts to find the privilege name on the local system.

### -param lpLuid [in]

A pointer to the LUID by which the privilege is known on the target system.

### -param lpName [out, optional]

A pointer to a buffer that receives a null-terminated string that represents the privilege name. For example, this string could be "SeSecurityPrivilege".

### -param cchName [in, out]

A pointer to a variable that specifies the size, in a <b>TCHAR</b> value, of the <i>lpName</i> buffer. When the function returns, this parameter contains the length of the privilege name, not including the terminating null character. If the buffer pointed to by the <i>lpName</i> parameter is too small, this variable contains the required size.

## -returns

If the function succeeds, the function returns nonzero.
						

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>LookupPrivilegeName</b> function supports only the privileges specified in the Defined Privileges section of Winnt.h. For a list of values, see <a href="/windows/desktop/SecAuthZ/privilege-constants">Privilege Constants</a>.





> [!NOTE]
> The winbase.h header defines LookupPrivilegeName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupprivilegedisplaynamea">LookupPrivilegeDisplayName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupprivilegevaluea">LookupPrivilegeValue</a>
