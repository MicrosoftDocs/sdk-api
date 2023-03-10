---
UID: NE:accctrl._ACCESS_MODE
title: ACCESS_MODE (accctrl.h)
description: Contains values that indicate how the access rights in an EXPLICIT_ACCESS structure apply to the trustee.
helpviewer_keywords: ["ACCESS_MODE","ACCESS_MODE enumeration [Security]","DENY_ACCESS","GRANT_ACCESS","NOT_USED_ACCESS","REVOKE_ACCESS","SET_ACCESS","SET_AUDIT_FAILURE","SET_AUDIT_SUCCESS","_win32_access_mode_str","accctrl/ACCESS_MODE","accctrl/DENY_ACCESS","accctrl/GRANT_ACCESS","accctrl/NOT_USED_ACCESS","accctrl/REVOKE_ACCESS","accctrl/SET_ACCESS","accctrl/SET_AUDIT_FAILURE","accctrl/SET_AUDIT_SUCCESS","security.access_mode"]
old-location: security\access_mode.htm
tech.root: security
ms.assetid: 52d1b3a3-eed5-4603-9056-520320da2a52
ms.date: 12/05/2018
ms.keywords: ACCESS_MODE, ACCESS_MODE enumeration [Security], DENY_ACCESS, GRANT_ACCESS, NOT_USED_ACCESS, REVOKE_ACCESS, SET_ACCESS, SET_AUDIT_FAILURE, SET_AUDIT_SUCCESS, _win32_access_mode_str, accctrl/ACCESS_MODE, accctrl/DENY_ACCESS, accctrl/GRANT_ACCESS, accctrl/NOT_USED_ACCESS, accctrl/REVOKE_ACCESS, accctrl/SET_ACCESS, accctrl/SET_AUDIT_FAILURE, accctrl/SET_AUDIT_SUCCESS, security.access_mode
req.header: accctrl.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACCESS_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACCESS_MODE
 - accctrl/_ACCESS_MODE
 - ACCESS_MODE
 - accctrl/ACCESS_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - ACCESS_MODE
---

# ACCESS_MODE enumeration


## -description

The <b>ACCESS_MODE</b> enumeration contains values that indicate how the access rights in an 
<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure apply to the trustee. Functions such as 
<a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a> and 
<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a> use these values to set or retrieve information in an <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE).

## -enum-fields

### -field NOT_USED_ACCESS

Value not used.

### -field GRANT_ACCESS

Indicates an 
<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a> structure. The new ACE combines the specified rights with any existing allowed or denied rights of the trustee.

### -field SET_ACCESS

Indicates an <a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a> structure that allows the specified rights. 




On input, this value discards any existing access control information for the trustee.

### -field DENY_ACCESS

Indicates an 
<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a> structure that denies the specified rights. 




On input, this value denies the specified rights in addition to any currently denied rights of the trustee.

### -field REVOKE_ACCESS

Indicates that all existing <a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a> or 
<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a> structures for the specified trustee are removed.

### -field SET_AUDIT_SUCCESS

Indicates a <a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a> structure that generates audit messages for successful attempts to use the specified access rights. 
						

On input, this value combines the specified rights with any existing audited access rights for the trustee.

### -field SET_AUDIT_FAILURE

Indicates a 
<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a> structure that generates audit messages for failed attempts to use the specified access rights.  

On input, this value combines the specified rights with any existing audited access rights for the trustee.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a>



<a href="/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a>