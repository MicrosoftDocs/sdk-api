---
UID: NS:guiddef._GUID
title: GUID
description: A GUID structure (guiddef.h) identifies an object such as a COM interfaces, or a COM class object, or a manager entry-point vector (EPV).
ms.date: 08/12/2022
ms.keywords: _GUID, GUID
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: guiddef.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: GUID
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - _GUID
 - guiddef/_GUID
 - GUID
 - guiddef/GUID
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - guiddef.h
api_name:
 - _GUID
 - GUID
---

## -description

A GUID identifies an object such as a COM interfaces, or a COM class object, or a manager entry-point vector (EPV). A GUID is a 128-bit value consisting of one group of 8 hexadecimal digits, followed by three groups of 4 hexadecimal digits each, followed by one group of 12 hexadecimal digits. The following example GUID shows the groupings of hexadecimal digits in a GUID: 6B29FC40-CA47-1067-B31D-00DD010662DA.

The **GUID** structure stores a GUID.

## -struct-fields

### -field Data1

Specifies the first 8 hexadecimal digits of the GUID.

### -field Data2

Specifies the first group of 4 hexadecimal digits.

### -field Data3

Specifies the second group of 4 hexadecimal digits.

### -field Data4

Array of 8 bytes. The first 2 bytes contain the third group of 4 hexadecimal digits. The remaining 6 bytes contain the final 12 hexadecimal digits.

## -remarks

GUIDs are the Microsoft implementation of the distributed computing environment (DCE) universally unique identifier ([UUID](/windows/win32/rpc/rpcdce/ns-rpcdce-uuid)). The RPC run-time libraries use UUIDs to check for compatibility between clients and servers and to select among multiple implementations of an interface. The Windows access-control functions use GUIDs to identify the type of object that an object-specific ACE in an access-control list (ACL) protects.

## See also

**ACCESS\_ALLOWED\_OBJECT\_ACE**  
**ACE**  
**ACL**  
[UUID](/windows/win32/rpc/rpcdce/ns-rpcdce-uuid)  
[UUID\_VECTOR](../rpcdce/ns-rpcdce-uuid_vector.md)
