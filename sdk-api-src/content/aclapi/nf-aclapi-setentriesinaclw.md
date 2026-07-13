---
UID: NF:aclapi.SetEntriesInAclW
title: SetEntriesInAclW function (aclapi.h)
description: Creates a new access control list (ACL) by merging new access control or audit control information into an existing ACL structure. (Unicode)
helpviewer_keywords: ["SetEntriesInAcl", "SetEntriesInAcl function [Security]", "SetEntriesInAclW", "_win32_setentriesinacl", "aclapi/SetEntriesInAcl", "aclapi/SetEntriesInAclW", "security.setentriesinacl"]
old-location: security\setentriesinacl.htm
tech.root: security
ms.assetid: 05960fc1-1ad2-4c19-a65c-62259af5e18c
ms.date: 12/05/2018
ms.keywords: SetEntriesInAcl, SetEntriesInAcl function [Security], SetEntriesInAclA, SetEntriesInAclW, _win32_setentriesinacl, aclapi/SetEntriesInAcl, aclapi/SetEntriesInAclA, aclapi/SetEntriesInAclW, security.setentriesinacl
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetEntriesInAclW (Unicode) and SetEntriesInAclA (ANSI)
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
 - SetEntriesInAclW
 - aclapi/SetEntriesInAclW
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
 - SetEntriesInAcl
 - SetEntriesInAclA
 - SetEntriesInAclW
---

# SetEntriesInAclW function


## -description

The <b>SetEntriesInAcl</b> function creates a new <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL) by merging new access control or audit control information into an existing 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure.

## -parameters

### -param cCountOfExplicitEntries [in]

The number of 
<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures in the <i>pListOfExplicitEntries</i> array.

### -param pListOfExplicitEntries [in, optional]

A pointer to an array of <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures that describe the access control information to merge into the existing ACL.

### -param OldAcl [in, optional]

A pointer to the existing ACL. This parameter can be <b>NULL</b>, in which case, the function creates a new ACL based on the <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> entries.

### -param NewAcl [out]

A pointer to a variable that receives a pointer to the new ACL. If the function succeeds, you must call the 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function to free the returned buffer.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.

## -remarks

Each entry in the array of <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structures specifies access control or audit control information for a specified trustee. A trustee can be a user, group, or other <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) value, such as a <a href="/windows/desktop/SecGloss/l-gly">logon identifier</a> or logon type (for instance, a Windows service or batch job). You can use a name or a SID to identify a trustee.

You can use the <b>SetEntriesInAcl</b> function to modify the list of <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) in a <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) or a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL). Note that <b>SetEntriesInAcl</b> does not prevent you from mixing access control and audit control information in the same 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>; however, the resulting ACL will contain meaningless entries.

For a DACL, the <b>grfAccessMode</b> member of the 
<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure specifies whether to allow, deny, or revoke access rights for the trustee. This member can specify one of the following values:

<ul>
<li>GRANT_ACCESS</li>
<li>SET_ACCESS</li>
<li>DENY_ACCESS</li>
<li>REVOKE_ACCESS</li>
</ul>
 For information about these values, see <a href="/windows/desktop/api/accctrl/ne-accctrl-access_mode">ACCESS_MODE</a>.

The <b>SetEntriesInAcl</b> function places any new access-denied ACEs at the beginning of the list of ACEs for the new 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>. This function  places any new access-allowed ACEs just before any existing access-allowed ACEs.

For a SACL, the <b>grfAccessMode</b> member of the 
<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure can specify the following values:

<ul>
<li>REVOKE_ACCESS</li>
<li>SET_AUDIT_FAILURE</li>
<li>SET_AUDIT_SUCCESS</li>
</ul>
SET_AUDIT_FAILURE and  SET_AUDIT_SUCCESS can be combined. For information about these values, see <a href="/windows/desktop/api/accctrl/ne-accctrl-access_mode">ACCESS_MODE</a>.

The <b>SetEntriesInAcl</b> function places any new system-audit ACEs at the beginning of the list of ACEs for the new ACL.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--">Modifying the ACLs of an Object</a> or <a href="/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--">Creating a Security Descriptor for a New Object</a> or <a href="/windows/desktop/SecAuthZ/taking-object-ownership-in-c--">Taking Object Ownership</a>.

<div class="code"></div>




> [!NOTE]
> The aclapi.h header defines SetEntriesInAcl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a>
