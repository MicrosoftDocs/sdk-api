---
UID: NS:winnt._ACCESS_DENIED_CALLBACK_ACE
title: ACCESS_DENIED_CALLBACK_ACE (winnt.h)
description: The ACCESS_DENIED_CALLBACK_ACE structure defines an access control entry for the discretionary access control list that controls access to an object.
helpviewer_keywords: ["*PACCESS_DENIED_CALLBACK_ACE","ACCESS_DENIED_CALLBACK_ACE","ACCESS_DENIED_CALLBACK_ACE structure [Security]","PACCESS_DENIED_CALLBACK_ACE","PACCESS_DENIED_CALLBACK_ACE structure pointer [Security]","_ACCESS_DENIED_CALLBACK_ACE","security.access_denied_callback_ace","winnt/ACCESS_DENIED_CALLBACK_ACE","winnt/PACCESS_DENIED_CALLBACK_ACE"]
old-location: security\access_denied_callback_ace.htm
tech.root: security
ms.assetid: 6df77b27-7aa3-455f-bffe-eeb90ba1bc15
ms.date: 12/05/2018
ms.keywords: '*PACCESS_DENIED_CALLBACK_ACE, ACCESS_DENIED_CALLBACK_ACE, ACCESS_DENIED_CALLBACK_ACE structure [Security], PACCESS_DENIED_CALLBACK_ACE, PACCESS_DENIED_CALLBACK_ACE structure pointer [Security], _ACCESS_DENIED_CALLBACK_ACE, security.access_denied_callback_ace, winnt/ACCESS_DENIED_CALLBACK_ACE, winnt/PACCESS_DENIED_CALLBACK_ACE'
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
req.typenames: ACCESS_DENIED_CALLBACK_ACE, *PACCESS_DENIED_CALLBACK_ACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACCESS_DENIED_CALLBACK_ACE
 - winnt/_ACCESS_DENIED_CALLBACK_ACE
 - PACCESS_DENIED_CALLBACK_ACE
 - winnt/PACCESS_DENIED_CALLBACK_ACE
 - ACCESS_DENIED_CALLBACK_ACE
 - winnt/ACCESS_DENIED_CALLBACK_ACE
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
 - ACCESS_DENIED_CALLBACK_ACE
---

# ACCESS_DENIED_CALLBACK_ACE structure


## -description

The <b>ACCESS_DENIED_CALLBACK_ACE</b> structure defines an  <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) for the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) that controls access to an object. An access-denied ACE denies access to an object for a specific <a href="/windows/desktop/SecGloss/t-gly">trustee</a> identified by a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

When the <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> function is called, each <b>ACCESS_DENIED_CALLBACK_ACE</b> structure contained in the DACL of a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure passed through a pointer to the <b>AuthzAccessCheck</b> function invokes a call to the application–defined <a href="/windows/desktop/SecAuthZ/authzaccesscheckcallback">AuthzAccessCheckCallback</a> function, in which a pointer to the <b>ACCESS_DENIED_CALLBACK_ACE</b> structure found is passed in the <i>pAce</i> parameter.

## -struct-fields

### -field Header

<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of ACE. It also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to ACCESS_DENIED_CALLBACK_ACE_TYPE, and the <b>AceSize</b> member should be set to the total number of bytes allocated for the <b>ACCESS_DENIED_CALLBACK_ACE</b> structure.

### -field Mask

Specifies an 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> structure that specifies the access rights explicitly denied by this ACE.

### -field SidStart

The first <b>DWORD</b> of a trustee's SID. The remaining bytes of the SID  are stored in contiguous memory after the <b>SidStart</b> member. This SID can be appended with application data.

## -remarks

<a href="/windows/desktop/SecAuthZ/ace">ACE structures</a> must be aligned on <b>DWORD</b> boundaries. All Windows memory-management functions return <b>DWORD</b>-aligned handles to memory.

The access rights specified by the <b>Mask</b> member are granted to any <a href="/windows/desktop/SecGloss/t-gly">trustee</a> that possesses an enabled SID that matches the SID stored in the <b>SidStart</b> member.

When an <b>ACCESS_DENIED_CALLBACK_ACE</b> structure is created, sufficient memory must be allocated to accommodate the complete SID of the trustee in the <b>SidStart</b> member and the contiguous memory that follows it.

## -see-also

<a href="/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace">AddAuditAccessObjectAce</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>