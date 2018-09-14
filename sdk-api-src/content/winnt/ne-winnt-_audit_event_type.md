---
UID: NE:winnt._AUDIT_EVENT_TYPE
title: "_AUDIT_EVENT_TYPE"
author: windows-sdk-content
description: Defines values that indicate the type of object being audited. The AccessCheckByTypeAndAuditAlarm and AccessCheckByTypeResultListAndAuditAlarm functions use these values.
old-location: security\audit_event_type.htm
tech.root: secauthz
ms.assetid: 7dc21840-6dcc-445b-a254-f8ca27008d63
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PAUDIT_EVENT_TYPE, AUDIT_EVENT_TYPE, AUDIT_EVENT_TYPE enumeration [Security], AuditEventDirectoryServiceAccess, AuditEventObjectAccess, PAUDIT_EVENT_TYPE, PAUDIT_EVENT_TYPE enumeration pointer [Security], _AUDIT_EVENT_TYPE, _win32_audit_event_type_str, security.audit_event_type, winnt/AUDIT_EVENT_TYPE, winnt/AuditEventDirectoryServiceAccess, winnt/AuditEventObjectAccess, winnt/PAUDIT_EVENT_TYPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - AUDIT_EVENT_TYPE
product: Windows
targetos: Windows
req.typenames: AUDIT_EVENT_TYPE, *PAUDIT_EVENT_TYPE
req.redist: 
---

# _AUDIT_EVENT_TYPE enumeration


## -description


The <b>AUDIT_EVENT_TYPE</b> enumeration type defines values that indicate the type of object being audited. The <a href="https://msdn.microsoft.com/ea14fd55-e0e4-4bf2-b20e-5874783c16c3">AccessCheckByTypeAndAuditAlarm</a> and <a href="https://msdn.microsoft.com/4b53a15a-5a6b-40c7-acf8-26b1f4bca4ae">AccessCheckByTypeResultListAndAuditAlarm</a> functions use these values.


## -enum-fields




### -field AuditEventObjectAccess

Indicates an object that generates audit messages only if the system administrator has enabled auditing access to files and objects.


### -field AuditEventDirectoryServiceAccess

Indicates a directory service object that generates audit messages only if the system administrator has enabled auditing access to directory service objects.


## -see-also




<a href="https://msdn.microsoft.com/ea14fd55-e0e4-4bf2-b20e-5874783c16c3">AccessCheckByTypeAndAuditAlarm</a>



<a href="https://msdn.microsoft.com/4b53a15a-5a6b-40c7-acf8-26b1f4bca4ae">AccessCheckByTypeResultListAndAuditAlarm</a>



<a href="https://msdn.microsoft.com/e2f22838-102e-432c-9c82-06a3e0741374">Authorization Enumerations</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>
 

 

