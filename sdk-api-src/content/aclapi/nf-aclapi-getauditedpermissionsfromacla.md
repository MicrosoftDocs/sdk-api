---
UID: NF:aclapi.GetAuditedPermissionsFromAclA
title: GetAuditedPermissionsFromAclA function (aclapi.h)
description: Retrieves the audited access rights for a specified trustee. (ANSI)
helpviewer_keywords: ["GetAuditedPermissionsFromAclA", "aclapi/GetAuditedPermissionsFromAclA"]
old-location: security\getauditedpermissionsfromacl.htm
tech.root: security
ms.assetid: 4381fe12-5fb3-4f9c-8daa-261cb1a466ec
ms.date: 12/05/2018
ms.keywords: GetAuditedPermissionsFromAcl, GetAuditedPermissionsFromAcl function [Security], GetAuditedPermissionsFromAclA, GetAuditedPermissionsFromAclW, _win32_getauditedpermissionsfromacl, aclapi/GetAuditedPermissionsFromAcl, aclapi/GetAuditedPermissionsFromAclA, aclapi/GetAuditedPermissionsFromAclW, security.getauditedpermissionsfromacl
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetAuditedPermissionsFromAclW (Unicode) and GetAuditedPermissionsFromAclA (ANSI)
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
 - GetAuditedPermissionsFromAclA
 - aclapi/GetAuditedPermissionsFromAclA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-trustee-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-security-trustee-l1-1-1.dll
 - advapi32legacy.dll
api_name:
 - GetAuditedPermissionsFromAcl
 - GetAuditedPermissionsFromAclA
 - GetAuditedPermissionsFromAclW
---

# GetAuditedPermissionsFromAclA function


## -description

The <b>GetAuditedPermissionsFromAcl</b> function retrieves the audited access rights for a specified trustee. The audited rights are based on the <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) of a specified <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL). The audited access rights indicate the types of access attempts that cause the system to generate an audit record in the system event log. The audited rights include those that the 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> specifies for the trustee or for any groups of which the trustee is a member. In determining the audited rights, the function does not consider the security privileges held by the trustee.

## -parameters

### -param pacl [in]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure from which to get the trustee's audited access rights.

### -param pTrustee [in]

A pointer to a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure that identifies the trustee. A trustee can be a user, group, or program (such as a Windows service). You can use a name or a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) to identify a trustee. For information about SID structures, see <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>.

### -param pSuccessfulAuditedRights [out]

A pointer to an 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> structure that receives the successful audit mask for rights audited for the trustee specified by the <i>pTrustee</i> parameter. The system generates an audit record when the trustee successfully uses any of these access rights.

### -param pFailedAuditRights [out]

A pointer to an <a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> structure that receives the failed audit mask for rights audited for the trustee specified by the <i>pTrustee</i> parameter. The system generates an audit record when the trustee fails in an attempt to use any of these rights.

## -returns

If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.

## -remarks

The <b>GetAuditedPermissionsFromAcl</b> function checks all system-audit ACEs in the ACL to determine the audited rights for the trustee. For all ACEs that specify audited rights for a group, <b>GetAuditedPermissionsFromAcl</b> enumerates the members of the group to determine whether the trustee is a member. The function returns an error if it cannot enumerate the members of a group.





> [!NOTE]
> The aclapi.h header defines GetAuditedPermissionsFromAcl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>



<a href="/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-geteffectiverightsfromacla">GetEffectiveRightsFromAcl</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>
