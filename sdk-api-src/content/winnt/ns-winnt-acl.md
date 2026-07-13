---
UID: NS:winnt._ACL
title: ACL (winnt.h)
description: Header of an access control list (ACL).
helpviewer_keywords: ["*PACL","ACL","ACL structure [Security]","PACL","PACL structure pointer [Security]","_ACL","_win32_acl_str","security.acl","winnt/ACL","winnt/PACL"]
old-location: security\acl.htm
tech.root: security
ms.assetid: 0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9
ms.date: 12/05/2018
ms.keywords: '*PACL, ACL, ACL structure [Security], PACL, PACL structure pointer [Security], _ACL, _win32_acl_str, security.acl, winnt/ACL, winnt/PACL'
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
req.typenames: ACL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACL
 - winnt/_ACL
 - ACL
 - winnt/ACL
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
 - ACL
---

# ACL structure


## -description

The <b>ACL</b> structure is the header of an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL). A complete ACL consists of an <b>ACL</b> structure followed by an ordered list of zero or more  <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs).

## -struct-fields

### -field AclRevision

Specifies the revision level of the ACL. This value should be ACL_REVISION, unless the ACL contains an object-specific ACE, in which case this value must be ACL_REVISION_DS. All ACEs in an ACL must be at the same revision level.

### -field Sbz1

Specifies a zero byte of <a href="/windows/desktop/SecGloss/p-gly">padding</a> that aligns the <b>AclRevision</b> member on a 16-bit boundary.

### -field AclSize

Specifies the size, in bytes, of the ACL. This value includes the **ACL** structure, all the ACEs, and the potential unused memory.

### -field AceCount

Specifies the number of ACEs stored in the ACL.

### -field Sbz2

Specifies two zero-bytes of <a href="/windows/desktop/SecGloss/p-gly">padding</a> that align the <b>ACL</b> structure on a 32-bit boundary.

## -remarks

An ACL includes a sequential list of zero or more ACEs. The individual ACEs in an ACL are numbered from 0 to <i>n</i>, where <i>n</i>+1 is the number of ACEs in the ACL. When editing an ACL, an application refers to an ACE within the ACL by the ACE's index.

There are two types of ACL: discretionary and system.

A <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) is controlled by the owner of an object or anyone granted WRITE_DAC access to the object. It specifies the access particular users and groups can have to an object. For example, the owner of a file can use a DACL to control which users and groups can and cannot have access to the file.

An object can also have system-level security information associated with it, in the form of a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) controlled by a system administrator. A SACL  allows the system administrator to audit any attempts to gain access to an object.

For a list of currently defined ACE structures, see <a href="/windows/desktop/SecAuthZ/ace">ACE</a>.

A fourth ACE structure, <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_ace">SYSTEM_ALARM_ACE</a>, is not currently supported.

The <b>ACL</b> structure is to be treated as though it were opaque and applications are not to attempt to work with its members directly. To ensure that ACLs are semantically correct, applications can use the functions listed in the See Also section to create and manipulate ACLs.

Each <b>ACL</b> and <a href="/windows/desktop/SecAuthZ/ace">ACE</a> structure begins on a <b>DWORD</b> boundary.

The maximum size for an ACL, including its ACEs, is 64 KB.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addace">AddAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-deleteace">DeleteAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl">GetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl">GetSecurityDescriptorSacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-initializeacl">InitializeAcl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidacl">IsValidAcl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setaclinformation">SetAclInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl">SetSecurityDescriptorDacl</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl">SetSecurityDescriptorSacl</a>