---
UID: NS:winnt._SYSTEM_AUDIT_CALLBACK_ACE
title: SYSTEM_AUDIT_CALLBACK_ACE (winnt.h)
description: The SYSTEM_AUDIT_CALLBACK_ACE structure defines an access control entry for the system access control list that specifies what types of access cause system-level notifications.
helpviewer_keywords: ["*PSYSTEM_AUDIT_CALLBACK_ACE","PACCESS_AUDIT_CALLBACK_ACE","PACCESS_AUDIT_CALLBACK_ACE structure pointer [Security]","SYSTEM_AUDIT_CALLBACK_ACE","SYSTEM_AUDIT_CALLBACK_ACE structure [Security]","_SYSTEM_AUDIT_CALLBACK_ACE","security.system_audit_callback_ace","winnt/PACCESS_AUDIT_CALLBACK_ACE","winnt/SYSTEM_AUDIT_CALLBACK_ACE"]
old-location: security\system_audit_callback_ace.htm
tech.root: security
ms.assetid: 4d1799b0-3e55-48d7-94ff-c0094945adea
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_AUDIT_CALLBACK_ACE, PACCESS_AUDIT_CALLBACK_ACE, PACCESS_AUDIT_CALLBACK_ACE structure pointer [Security], SYSTEM_AUDIT_CALLBACK_ACE, SYSTEM_AUDIT_CALLBACK_ACE structure [Security], _SYSTEM_AUDIT_CALLBACK_ACE, security.system_audit_callback_ace, winnt/PACCESS_AUDIT_CALLBACK_ACE, winnt/SYSTEM_AUDIT_CALLBACK_ACE'
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SYSTEM_AUDIT_CALLBACK_ACE, *PSYSTEM_AUDIT_CALLBACK_ACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_AUDIT_CALLBACK_ACE
 - winnt/_SYSTEM_AUDIT_CALLBACK_ACE
 - PSYSTEM_AUDIT_CALLBACK_ACE
 - winnt/PSYSTEM_AUDIT_CALLBACK_ACE
 - SYSTEM_AUDIT_CALLBACK_ACE
 - winnt/SYSTEM_AUDIT_CALLBACK_ACE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SYSTEM_AUDIT_CALLBACK_ACE
---

# SYSTEM_AUDIT_CALLBACK_ACE structure


## -description

The <b>SYSTEM_AUDIT_CALLBACK_ACE</b> structure defines an <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) for the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) that specifies what types of access cause system-level notifications. A system-audit ACE causes an audit message to be logged when a specified <a href="/windows/desktop/SecGloss/t-gly">trustee</a> attempts to gain access to an object. The trustee is identified by a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

When the <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> function is called, each <b>SYSTEM_AUDIT_CALLBACK_ACE</b> structure contained in the DACL of a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure passed through a pointer to the <b>AuthzAccessCheck</b> function invokes a call to the application-defined <a href="/windows/desktop/SecAuthZ/authzaccesscheckcallback">AuthzAccessCheckCallback</a> function, in which a pointer to the <b>SYSTEM_AUDIT_CALLBACK_ACE</b> structure found is passed in the <i>pAce</i> parameter.

## -struct-fields

### -field Header

<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of ACE. It also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to SYSTEM_AUDIT_CALLBACK_ACE_TYPE, and the <b>AceSize</b> member should be set to the total number of bytes allocated for the <b>SYSTEM_AUDIT_CALLBACK_ACE</b> structure.

### -field Mask

Specifies an 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> structure that gives the access rights that cause audit messages to be generated. The SUCCESSFUL_ACCESS_ACE_FLAG and FAILED_ACCESS_ACE_FLAG flags in the <b>AceFlags</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure indicate whether messages are generated for successful access attempts, unsuccessful access attempts, or both.

### -field SidStart

The first <b>DWORD</b> of a trustee's SID. The remaining bytes of the SID  are stored in contiguous memory after the <b>SidStart</b> member. This SID can be appended with application data.

## -remarks

ACE structures must be aligned on <b>DWORD</b> boundaries. All Windows memory-management functions return <b>DWORD</b>-aligned handles to memory.

When a <b>SYSTEM_AUDIT_CALLBACK_ACE</b> structure is created, sufficient memory must be allocated to accommodate the complete SID of the trustee in the <b>SidStart</b> member and the contiguous memory that follows it.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace">AddAuditAccessObjectAce</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>