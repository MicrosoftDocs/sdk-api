---
UID: NE:winevt._EVT_VARIANT_TYPE
title: EVT_VARIANT_TYPE (winevt.h)
description: Defines the possible data types of a variant data item.
helpviewer_keywords: ["EVT_VARIANT_TYPE","EvtVarTypeAnsiString","EvtVarTypeBinary","EvtVarTypeBoolean","EvtVarTypeByte","EvtVarTypeDouble","EvtVarTypeEvtHandle","EvtVarTypeEvtXml","EvtVarTypeFileTime","EvtVarTypeGuid","EvtVarTypeHexInt32","EvtVarTypeHexInt64","EvtVarTypeInt16","EvtVarTypeInt32","EvtVarTypeInt64","EvtVarTypeNull","EvtVarTypeSByte","EvtVarTypeSid","EvtVarTypeSingle","EvtVarTypeSizeT","EvtVarTypeString","EvtVarTypeSysTime","EvtVarTypeUInt16","EvtVarTypeUInt32","EvtVarTypeUInt64","_EVT_VARIANT_TYPE","_EVT_VARIANT_TYPE enumeration [EventLog]","wes.evt_variant_type","winevt/EvtVarTypeAnsiString","winevt/EvtVarTypeBinary","winevt/EvtVarTypeBoolean","winevt/EvtVarTypeByte","winevt/EvtVarTypeDouble","winevt/EvtVarTypeEvtHandle","winevt/EvtVarTypeEvtXml","winevt/EvtVarTypeFileTime","winevt/EvtVarTypeGuid","winevt/EvtVarTypeHexInt32","winevt/EvtVarTypeHexInt64","winevt/EvtVarTypeInt16","winevt/EvtVarTypeInt32","winevt/EvtVarTypeInt64","winevt/EvtVarTypeNull","winevt/EvtVarTypeSByte","winevt/EvtVarTypeSid","winevt/EvtVarTypeSingle","winevt/EvtVarTypeSizeT","winevt/EvtVarTypeString","winevt/EvtVarTypeSysTime","winevt/EvtVarTypeUInt16","winevt/EvtVarTypeUInt32","winevt/EvtVarTypeUInt64","winevt/_EVT_VARIANT_TYPE"]
old-location: wes\evt_variant_type.htm
tech.root: wes
ms.assetid: 13cf5e71-07bb-45ac-89f9-b76a26539dcd
ms.date: 12/05/2018
ms.keywords: EVT_VARIANT_TYPE, EvtVarTypeAnsiString, EvtVarTypeBinary, EvtVarTypeBoolean, EvtVarTypeByte, EvtVarTypeDouble, EvtVarTypeEvtHandle, EvtVarTypeEvtXml, EvtVarTypeFileTime, EvtVarTypeGuid, EvtVarTypeHexInt32, EvtVarTypeHexInt64, EvtVarTypeInt16, EvtVarTypeInt32, EvtVarTypeInt64, EvtVarTypeNull, EvtVarTypeSByte, EvtVarTypeSid, EvtVarTypeSingle, EvtVarTypeSizeT, EvtVarTypeString, EvtVarTypeSysTime, EvtVarTypeUInt16, EvtVarTypeUInt32, EvtVarTypeUInt64, _EVT_VARIANT_TYPE, _EVT_VARIANT_TYPE enumeration [EventLog], wes.evt_variant_type, winevt/EvtVarTypeAnsiString, winevt/EvtVarTypeBinary, winevt/EvtVarTypeBoolean, winevt/EvtVarTypeByte, winevt/EvtVarTypeDouble, winevt/EvtVarTypeEvtHandle, winevt/EvtVarTypeEvtXml, winevt/EvtVarTypeFileTime, winevt/EvtVarTypeGuid, winevt/EvtVarTypeHexInt32, winevt/EvtVarTypeHexInt64, winevt/EvtVarTypeInt16, winevt/EvtVarTypeInt32, winevt/EvtVarTypeInt64, winevt/EvtVarTypeNull, winevt/EvtVarTypeSByte, winevt/EvtVarTypeSid, winevt/EvtVarTypeSingle, winevt/EvtVarTypeSizeT, winevt/EvtVarTypeString, winevt/EvtVarTypeSysTime, winevt/EvtVarTypeUInt16, winevt/EvtVarTypeUInt32, winevt/EvtVarTypeUInt64, winevt/_EVT_VARIANT_TYPE
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EVT_VARIANT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_VARIANT_TYPE
 - winevt/_EVT_VARIANT_TYPE
 - EVT_VARIANT_TYPE
 - winevt/EVT_VARIANT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEvt.h
api_name:
 - EVT_VARIANT_TYPE
---

# EVT_VARIANT_TYPE enumeration


## -description

Defines the possible data types of a variant data item.

## -enum-fields

### -field EvtVarTypeNull:0

Null content that implies that the element that contains the content does not exist.

### -field EvtVarTypeString:1

A null-terminated Unicode string.

### -field EvtVarTypeAnsiString:2

A null-terminated ANSI string.

### -field EvtVarTypeSByte:3

A signed 8-bit integer value.

### -field EvtVarTypeByte:4

An unsigned 8-bit integer value.

### -field EvtVarTypeInt16:5

An signed 16-bit integer value.

### -field EvtVarTypeUInt16:6

An unsigned 16-bit integer value.

### -field EvtVarTypeInt32:7

A signed 32-bit integer value.

### -field EvtVarTypeUInt32:8

An unsigned 32-bit integer value.

### -field EvtVarTypeInt64:9

A signed 64-bit integer value.

### -field EvtVarTypeUInt64:10

An unsigned 64-bit integer value.

### -field EvtVarTypeSingle:11

A single-precision real value.

### -field EvtVarTypeDouble:12

A double-precision real value.

### -field EvtVarTypeBoolean:13

A Boolean value.

### -field EvtVarTypeBinary:14

A hexadecimal binary value.

### -field EvtVarTypeGuid:15

A GUID value.

### -field EvtVarTypeSizeT:16

An unsigned 32-bit or 64-bit integer value that contains a pointer address.

### -field EvtVarTypeFileTime:17

A FILETIME value.

### -field EvtVarTypeSysTime:18

 A SYSTEMTIME value.

### -field EvtVarTypeSid:19

A security identifier (<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>) structure

### -field EvtVarTypeHexInt32:20

A 32-bit hexadecimal number.

### -field EvtVarTypeHexInt64:21

A 64-bit hexadecimal number.

### -field EvtVarTypeEvtHandle:32

An EVT_HANDLE value.

### -field EvtVarTypeEvtXml:35

A null-terminated Unicode string that contains XML.

## -see-also

<a href="/windows/desktop/api/winevt/ns-winevt-evt_variant">EVT_VARIANT</a>
