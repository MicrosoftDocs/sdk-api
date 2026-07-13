---
UID: NF:winbase.LookupPrivilegeDisplayNameA
title: LookupPrivilegeDisplayNameA function (winbase.h)
description: Retrieves the display name that represents a specified privilege. (ANSI)
helpviewer_keywords: ["LookupPrivilegeDisplayNameA", "winbase/LookupPrivilegeDisplayNameA"]
old-location: security\lookupprivilegedisplayname.htm
tech.root: security
ms.assetid: 1fbb26b6-615e-4883-9f4b-3a1d05d9feaa
ms.date: 12/05/2018
ms.keywords: LookupPrivilegeDisplayName, LookupPrivilegeDisplayName function [Security], LookupPrivilegeDisplayNameA, LookupPrivilegeDisplayNameW, _win32_lookupprivilegedisplayname, security.lookupprivilegedisplayname, winbase/LookupPrivilegeDisplayName, winbase/LookupPrivilegeDisplayNameA, winbase/LookupPrivilegeDisplayNameW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LookupPrivilegeDisplayNameW (Unicode) and LookupPrivilegeDisplayNameA (ANSI)
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
 - LookupPrivilegeDisplayNameA
 - winbase/LookupPrivilegeDisplayNameA
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
 - LookupPrivilegeDisplayName
 - LookupPrivilegeDisplayNameA
 - LookupPrivilegeDisplayNameW
---

# LookupPrivilegeDisplayNameA function


## -description

The <b>LookupPrivilegeDisplayName</b> function retrieves the display name that represents a specified privilege.

## -parameters

### -param lpSystemName [in, optional]

A pointer to a null-terminated string that specifies the name of the system on which the  privilege name is retrieved. If a null string is specified, the function attempts to find the display name on the local system.

### -param lpName [in]

A pointer to a null-terminated string that specifies the name of the privilege, as defined in Winnt.h. For example, this parameter could specify the constant, SE_REMOTE_SHUTDOWN_NAME, or its corresponding string, "SeRemoteShutdownPrivilege". For a list of values, see <a href="/windows/desktop/SecAuthZ/privilege-constants">Privilege Constants</a>.

### -param lpDisplayName [out, optional]

A pointer to a buffer that receives a null-terminated string that specifies the privilege display name. For example, if the <i>lpName</i> parameter is SE_REMOTE_SHUTDOWN_NAME, the privilege display name is "Force shutdown from a remote system."

### -param cchDisplayName [in, out]

A pointer to a variable that specifies the size, in <b>TCHAR</b>s, of the <i>lpDisplayName</i> buffer. When the function returns, this parameter contains the length of the privilege display name, not including the terminating null character. If the buffer pointed to by the <i>lpDisplayName</i> parameter is too small, this variable contains the required size.

### -param lpLanguageId [out]

A pointer to a variable that receives the language identifier for the returned display name.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>LookupPrivilegeDisplayName</b> function retrieves display names only for the privileges specified in the Defined Privileges section of Winnt.h.





> [!NOTE]
> The winbase.h header defines LookupPrivilegeDisplayName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupprivilegenamea">LookupPrivilegeName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-lookupprivilegevaluea">LookupPrivilegeValue</a>
