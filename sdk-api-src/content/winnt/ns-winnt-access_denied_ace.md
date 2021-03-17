---
UID: NS:winnt._ACCESS_DENIED_ACE
title: ACCESS_DENIED_ACE (winnt.h)
description: Defines an access control entry (ACE) for the discretionary access control list (DACL) that controls access to an object. An access-denied ACE denies access to an object for a specific trustee identified by a security identifier (SID).
helpviewer_keywords: ["*PACCESS_DENIED_ACE","ACCESS_DENIED_ACE","ACCESS_DENIED_ACE structure [Security]","PACCESS_DENIED_ACE","PACCESS_DENIED_ACE structure pointer [Security]","_ACCESS_DENIED_ACE","_win32_access_denied_ace_str","security.access_denied_ace","winnt/ACCESS_DENIED_ACE","winnt/PACCESS_DENIED_ACE"]
old-location: security\access_denied_ace.htm
tech.root: security
ms.assetid: d76a92d0-ccd0-4e73-98b6-43bcd661134d
ms.date: 12/05/2018
ms.keywords: '*PACCESS_DENIED_ACE, ACCESS_DENIED_ACE, ACCESS_DENIED_ACE structure [Security], PACCESS_DENIED_ACE, PACCESS_DENIED_ACE structure pointer [Security], _ACCESS_DENIED_ACE, _win32_access_denied_ace_str, security.access_denied_ace, winnt/ACCESS_DENIED_ACE, winnt/PACCESS_DENIED_ACE'
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
req.typenames: ACCESS_DENIED_ACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACCESS_DENIED_ACE
 - winnt/_ACCESS_DENIED_ACE
 - ACCESS_DENIED_ACE
 - winnt/ACCESS_DENIED_ACE
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
 - ACCESS_DENIED_ACE
---

# ACCESS_DENIED_ACE structure


## -description

The <b>ACCESS_DENIED_ACE</b> structure defines an  <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) for the  <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) that controls access to an object. An access-denied  ACE denies access to an object for a specific <a href="/windows/desktop/SecGloss/t-gly">trustee</a> identified by a  <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

## -struct-fields

### -field Header

An <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of ACE. It also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to ACCESS_DENIED_ACE_TYPE, and the <b>AceSize</b> member should be set to the total number of bytes allocated for the <b>ACCESS_DENIED_ACE</b> structure.

### -field Mask

An 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> structure that specifies the access rights explicitly denied by this ACE.

### -field SidStart

 The first <b>DWORD</b> of a trustee's SID. The remaining bytes of the SID  are stored in contiguous memory after the <b>SidStart</b> member. This SID can be appended with application data.

## -remarks

<a href="/windows/desktop/SecAuthZ/ace">ACE structures</a> must be aligned on <b>DWORD</b> boundaries. All Windows memory-management functions return <b>DWORD</b>-aligned handles to memory.

The access rights specified by the <b>Mask</b> member are denied to any <a href="/windows/desktop/SecGloss/t-gly">trustee</a> that possesses an enabled SID that matches the SID stored in the <b>SidStart</b> member.

An <b>ACCESS_DENIED_ACE</b> structure can be created in an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL) by a call to the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace">AddAccessDeniedAce</a> or <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedaceex">AddAccessDeniedAceEx</a> function. When these functions are used, the correct amount of memory needed to accommodate the trustee's SID is allocated and the values of the <b>Header.AceType</b> and <b>Header.AceSize</b> members are set automatically. If the <b>AddAccessDeniedAceEx</b> function is used, the <b>Header.AceFlags</b> member is also set. When an <b>ACCESS_DENIED_ACE</b> structure is created outside an ACL, sufficient memory must be allocated to accommodate the complete SID of the trustee in the <b>SidStart</b> member and the contiguous memory following it, and the values of the <b>Header.AceType</b>, <b>Header.AceFlags</b>, and <b>Header.AceSize</b> members must be set explicitly by the application.

## -see-also

<a href="/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace">AddAccessDeniedAce</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>