---
UID: NE:winnt._AUDIT_EVENT_TYPE
title: AUDIT_EVENT_TYPE (winnt.h)
description: Defines values that indicate the type of object being audited. The AccessCheckByTypeAndAuditAlarm and AccessCheckByTypeResultListAndAuditAlarm functions use these values.
helpviewer_keywords: ["*PAUDIT_EVENT_TYPE","AUDIT_EVENT_TYPE","AUDIT_EVENT_TYPE enumeration [Security]","AuditEventDirectoryServiceAccess","AuditEventObjectAccess","PAUDIT_EVENT_TYPE","PAUDIT_EVENT_TYPE enumeration pointer [Security]","_win32_audit_event_type_str","security.audit_event_type","winnt/AUDIT_EVENT_TYPE","winnt/AuditEventDirectoryServiceAccess","winnt/AuditEventObjectAccess","winnt/PAUDIT_EVENT_TYPE"]
old-location: security\audit_event_type.htm
tech.root: security
ms.assetid: 7dc21840-6dcc-445b-a254-f8ca27008d63
ms.date: 12/05/2018
ms.keywords: '*PAUDIT_EVENT_TYPE, AUDIT_EVENT_TYPE, AUDIT_EVENT_TYPE enumeration [Security], AuditEventDirectoryServiceAccess, AuditEventObjectAccess, PAUDIT_EVENT_TYPE, PAUDIT_EVENT_TYPE enumeration pointer [Security], _win32_audit_event_type_str, security.audit_event_type, winnt/AUDIT_EVENT_TYPE, winnt/AuditEventDirectoryServiceAccess, winnt/AuditEventObjectAccess, winnt/PAUDIT_EVENT_TYPE'
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
req.typenames: AUDIT_EVENT_TYPE, *PAUDIT_EVENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUDIT_EVENT_TYPE
 - winnt/_AUDIT_EVENT_TYPE
 - PAUDIT_EVENT_TYPE
 - winnt/PAUDIT_EVENT_TYPE
 - AUDIT_EVENT_TYPE
 - winnt/AUDIT_EVENT_TYPE
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
 - AUDIT_EVENT_TYPE
---

# AUDIT_EVENT_TYPE enumeration


## -description

The <b>AUDIT_EVENT_TYPE</b> enumeration type defines values that indicate the type of object being audited. The <a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytypeandauditalarma">AccessCheckByTypeAndAuditAlarm</a> and <a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma">AccessCheckByTypeResultListAndAuditAlarm</a> functions use these values.

## -enum-fields

### -field AuditEventObjectAccess

Indicates an object that generates audit messages only if the system administrator has enabled auditing access to files and objects.

### -field AuditEventDirectoryServiceAccess

Indicates a directory service object that generates audit messages only if the system administrator has enabled auditing access to directory service objects.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytypeandauditalarma">AccessCheckByTypeAndAuditAlarm</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma">AccessCheckByTypeResultListAndAuditAlarm</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>