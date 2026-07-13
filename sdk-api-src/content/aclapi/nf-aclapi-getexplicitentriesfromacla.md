---
UID: NF:aclapi.GetExplicitEntriesFromAclA
title: GetExplicitEntriesFromAclA function (aclapi.h)
description: Retrieves an array of structures that describe the access control entries (ACEs) in an access control list (ACL). (ANSI)
helpviewer_keywords: ["GetExplicitEntriesFromAclA", "aclapi/GetExplicitEntriesFromAclA"]
old-location: security\getexplicitentriesfromacl.htm
tech.root: security
ms.assetid: 186aa6aa-efc3-4f8a-acad-e257da3dac0b
ms.date: 12/05/2018
ms.keywords: GetExplicitEntriesFromAcl, GetExplicitEntriesFromAcl function [Security], GetExplicitEntriesFromAclA, GetExplicitEntriesFromAclW, _win32_getexplicitentriesfromacl, aclapi/GetExplicitEntriesFromAcl, aclapi/GetExplicitEntriesFromAclA, aclapi/GetExplicitEntriesFromAclW, security.getexplicitentriesfromacl
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetExplicitEntriesFromAclW (Unicode) and GetExplicitEntriesFromAclA (ANSI)
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
 - GetExplicitEntriesFromAclA
 - aclapi/GetExplicitEntriesFromAclA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-Provider-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-DownLevel-AdvApi32-l3-1-0.dll
 - ntmarta.dll
 - API-MS-Win-Security-Provider-Ansi-L1-1-0.dll
api_name:
 - GetExplicitEntriesFromAcl
 - GetExplicitEntriesFromAclA
 - GetExplicitEntriesFromAclW
---

# GetExplicitEntriesFromAclA function


## -description

The <b>GetExplicitEntriesFromAcl</b> function retrieves an array of structures that describe the <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) in an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

## -parameters

### -param pacl [in]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure from which to get 
<a href="/windows/desktop/SecAuthZ/ace">ACE</a> information.

### -param pcCountOfExplicitEntries [out]

A pointer to a variable that receives the number of <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures returned in the <i>pListOfExplicitEntries</i> array.

### -param pListOfExplicitEntries [out]

A pointer to a variable that receives a pointer to an array of <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures that describe the ACEs in the ACL. If the function succeeds, you must call the 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function to free the returned buffer.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.

## -remarks

Each entry in the array of 
<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures describes access control information from an 
<a href="/windows/desktop/SecAuthZ/ace">ACE</a> for a trustee. A trustee can be a user, group, or program (such as a Windows service).

Each <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure specifies a set of access rights and an access mode flag that indicates whether the ACE allows, denies, or audits the specified rights.

For a <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL), the access mode flag can be  either GRANT_ACCESS or DENY_ACCESS. For information about these values, see <a href="/windows/desktop/api/accctrl/ne-accctrl-access_mode">ACCESS_MODE</a>.

For a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL), the access mode flag can be SET_AUDIT_ACCESS, SET_AUDIT_FAILURE, or both. For information about these values, see <a href="/windows/desktop/api/accctrl/ne-accctrl-access_mode">ACCESS_MODE</a>.





> [!NOTE]
> The aclapi.h header defines GetExplicitEntriesFromAcl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-access_mode">ACCESS_MODE</a>



<a href="/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a>
