---
UID: NE:adtgen._AUDIT_PARAM_TYPE
title: AUDIT_PARAM_TYPE (adtgen.h)
description: Defines the type of audit parameters that are available.
helpviewer_keywords: ["APT_Guid","APT_Int64","APT_IpAddress","APT_LogonId","APT_LogonIdWithSid","APT_Luid","APT_None","APT_ObjectTypeList","APT_Pointer","APT_Sid","APT_String","APT_Time","APT_Ulong","AUDIT_PARAM_TYPE","AUDIT_PARAM_TYPE enumeration [Security]","adtgen/APT_Guid","adtgen/APT_Int64","adtgen/APT_IpAddress","adtgen/APT_LogonId","adtgen/APT_LogonIdWithSid","adtgen/APT_Luid","adtgen/APT_None","adtgen/APT_ObjectTypeList","adtgen/APT_Pointer","adtgen/APT_Sid","adtgen/APT_String","adtgen/APT_Time","adtgen/APT_Ulong","adtgen/AUDIT_PARAM_TYPE","security.audit_param_type"]
old-location: security\audit_param_type.htm
tech.root: security
ms.assetid: 1ECC866A-2DD3-4EE4-B2CC-7F5ADF7FFC99
ms.date: 12/05/2018
ms.keywords: APT_Guid, APT_Int64, APT_IpAddress, APT_LogonId, APT_LogonIdWithSid, APT_Luid, APT_None, APT_ObjectTypeList, APT_Pointer, APT_Sid, APT_String, APT_Time, APT_Ulong, AUDIT_PARAM_TYPE, AUDIT_PARAM_TYPE enumeration [Security], adtgen/APT_Guid, adtgen/APT_Int64, adtgen/APT_IpAddress, adtgen/APT_LogonId, adtgen/APT_LogonIdWithSid, adtgen/APT_Luid, adtgen/APT_None, adtgen/APT_ObjectTypeList, adtgen/APT_Pointer, adtgen/APT_Sid, adtgen/APT_String, adtgen/APT_Time, adtgen/APT_Ulong, adtgen/AUDIT_PARAM_TYPE, security.audit_param_type
req.header: adtgen.h
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
req.typenames: AUDIT_PARAM_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUDIT_PARAM_TYPE
 - adtgen/_AUDIT_PARAM_TYPE
 - AUDIT_PARAM_TYPE
 - adtgen/AUDIT_PARAM_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Adtgen.h
api_name:
 - AUDIT_PARAM_TYPE
---

# AUDIT_PARAM_TYPE enumeration


## -description

The <b>AUDIT_PARAM_TYPE</b> enumeration defines the type of audit parameters that are available.

## -enum-fields

### -field APT_None

No audit options.

### -field APT_String

A string that terminates with <b>NULL</b>.

### -field APT_Ulong

An unsigned long.

### -field APT_Pointer

A pointer that is used to specify handles and pointers. These are 32-bit on 32-bit systems and 64-bit on 64-bit systems. Use this option when you are interested in the absolute value of the pointer. The memory to which the pointer points is not marshaled when using this type.

### -field APT_Sid

The <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

### -field APT_LogonId

The logon identifier (LUID) that results in three output parameters:

<ul>
<li>Account name</li>
<li>Authority name</li>
<li>LogonID""</li>
</ul>

### -field APT_ObjectTypeList

Object type list.

### -field APT_Luid

LUID that is not translated to LogonId.

### -field APT_Guid

GUID.

### -field APT_Time

Time as FILETIME.

### -field APT_Int64

ULONGLONG.

### -field APT_IpAddress

IP Address (IPv4 and IPv6). This logs the address as the first parameter and the port as the second parameter. You must ensure that two entries are added in the event message file. You should ensure that the buffer size is 128 bytes.

### -field APT_LogonIdWithSid

Logon ID with SID that results in four output parameters:

<ul>
<li>SID</li>
<li>Account name</li>
<li>Authority name</li>
<li>LogonID</li>
</ul>