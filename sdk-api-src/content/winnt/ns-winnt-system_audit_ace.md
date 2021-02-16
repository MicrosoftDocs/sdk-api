---
UID: NS:winnt._SYSTEM_AUDIT_ACE
title: SYSTEM_AUDIT_ACE (winnt.h)
description: Defines an access control entry (ACE) for the system access control list (SACL) that specifies what types of access cause system-level notifications.
helpviewer_keywords: ["*PSYSTEM_AUDIT_ACE","PSYSTEM_AUDIT_ACE","PSYSTEM_AUDIT_ACE structure pointer [Security]","SYSTEM_AUDIT_ACE","SYSTEM_AUDIT_ACE structure [Security]","_SYSTEM_AUDIT_ACE","_win32_system_audit_ace_str","security.system_audit_ace","winnt/PSYSTEM_AUDIT_ACE","winnt/SYSTEM_AUDIT_ACE"]
old-location: security\system_audit_ace.htm
tech.root: security
ms.assetid: c26b5856-5447-4606-8110-f24a4d235c64
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_AUDIT_ACE, PSYSTEM_AUDIT_ACE, PSYSTEM_AUDIT_ACE structure pointer [Security], SYSTEM_AUDIT_ACE, SYSTEM_AUDIT_ACE structure [Security], _SYSTEM_AUDIT_ACE, _win32_system_audit_ace_str, security.system_audit_ace, winnt/PSYSTEM_AUDIT_ACE, winnt/SYSTEM_AUDIT_ACE'
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
req.typenames: SYSTEM_AUDIT_ACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_AUDIT_ACE
 - winnt/_SYSTEM_AUDIT_ACE
 - SYSTEM_AUDIT_ACE
 - winnt/SYSTEM_AUDIT_ACE
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
 - SYSTEM_AUDIT_ACE
---

# SYSTEM_AUDIT_ACE structure


## -description

The <b>SYSTEM_AUDIT_ACE</b> structure defines an  <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) for the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) that specifies what types of access cause system-level notifications. A system-audit ACE causes an audit message to be logged when a specified <a href="/windows/desktop/SecGloss/t-gly">trustee</a> attempts to gain access to an object. The trustee is identified by a  <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

## -struct-fields

### -field Header

<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of ACE. It also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to SYSTEM_AUDIT_ACE_TYPE, and the <b>AceSize</b> member should be set to the total number of bytes allocated for the <b>SYSTEM_AUDIT_ACE</b> structure.

### -field Mask

Specifies an 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> structure that gives the access rights that cause audit messages to be generated. The SUCCESSFUL_ACCESS_ACE_FLAG and FAILED_ACCESS_ACE_FLAG flags in the <b>AceFlags</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure indicate whether messages are generated for successful access attempts, unsuccessful access attempts, or both.

### -field SidStart

The first <b>DWORD</b> of a  trustee's SID. The remaining bytes of the SID  are stored in contiguous memory after the <b>SidStart</b> member. This SID can be appended with application data. 

An access attempt of a kind specified by the <b>Mask</b> member by any trustee whose SID matches the <b>SidStart</b> member causes the system to generate an audit message. If an application does not specify a SID for this member, audit messages are generated for the specified access rights for all trustees.

## -remarks

Audit messages are stored in an event log that can be manipulated by using the Windows API event-logging functions or by using the Event Viewer (Eventvwr.exe).

ACE structures should be aligned on <b>DWORD</b> boundaries. All Windows memory-management functions return <b>DWORD</b>-aligned handles to memory.

When a <b>SYSTEM_AUDIT_ACE</b> structure is created, sufficient memory must be allocated to accommodate the complete SID of the trustee in the <b>SidStart</b> member and the contiguous memory that follows it.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>