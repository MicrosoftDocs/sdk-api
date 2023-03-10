---
UID: NS:dbt._DEV_BROADCAST_USERDEFINED
title: _DEV_BROADCAST_USERDEFINED (dbt.h)
description: Contains the user-defined event and optional data associated with the DBT_USERDEFINED device event.
helpviewer_keywords: ["_DEV_BROADCAST_USERDEFINED","_DEV_BROADCAST_USERDEFINED structure","_win32__dev_broadcast_userdefined_str","base._dev_broadcast_userdefined_str","dbt/_DEV_BROADCAST_USERDEFINED"]
old-location: base\_dev_broadcast_userdefined_str.htm
tech.root: base
ms.assetid: e90fbce2-cae7-4e78-b6f5-82b200390cb7
ms.date: 12/05/2018
ms.keywords: _DEV_BROADCAST_USERDEFINED, _DEV_BROADCAST_USERDEFINED structure, _win32__dev_broadcast_userdefined_str, base._dev_broadcast_userdefined_str, dbt/_DEV_BROADCAST_USERDEFINED
req.header: dbt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEV_BROADCAST_USERDEFINED
 - dbt/_DEV_BROADCAST_USERDEFINED
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dbt.h
api_name:
 - _DEV_BROADCAST_USERDEFINED
---

# _DEV_BROADCAST_USERDEFINED structure


## -description

Contains the user-defined event and optional data associated with the 
<a href="/windows/desktop/DevIO/dbt-userdefined">DBT_USERDEFINED</a> device event.

## -struct-fields

### -field dbud_dbh

Information about the device affected by a 
<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a> message as specified by the 
<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_hdr">DEV_BROADCAST_HDR</a> structure. Because 
<b>_DEV_BROADCAST_USERDEFINED</b> is variable length, the <b>dbch_size</b> member of the <b>dbud_dbh</b> structure must be the size in bytes of the entire structure, including the variable length portion.

### -field dbud_szName

A pointer to a case-sensitive, null-terminated string that names the message. The string must consist of the vendor name, a backslash, followed by arbitrary user-defined null-terminated text.

## -remarks

Because this structure contains variable length fields, use it as a template for creating a pointer to a user-defined structure. Note that the structure must not contain pointers. The following example shows such a user-defined structure.


```cpp
#define NAME_LENGTH 32 
#define USER_LENGTH 50 
 
typedef struct tagWIDGET_WARE_DEV_BROADCAST_USERDEFINED
{
    struct _DEV_BROADCAST_HDR DBHeader; 
    char   szName[NAME_LENGTH];
    BYTE   UserDefined[USER_LENGTH]; 
} WIDGET_WARE_DEV_BROADCAST_USERDEFINED;
```

## -see-also

<a href="/windows/desktop/DevIO/dbt-userdefined">DBT_USERDEFINED</a>



<a href="/windows/desktop/api/dbt/ns-dbt-dev_broadcast_hdr">DEV_BROADCAST_HDR</a>



<a href="/windows/desktop/DevIO/wm-devicechange">WM_DEVICECHANGE</a>