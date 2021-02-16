---
UID: NS:winevt._EVT_VARIANT
title: EVT_VARIANT (winevt.h)
description: Contains event data or property values.
helpviewer_keywords: ["*PEVT_VARIANT","EVT_VARIANT","EVT_VARIANT structure [EventLog]","PEVT_VARIANT","PEVT_VARIANT structure pointer [EventLog]","wes.evt_variant","winevt/PEVT_VARIANT","winevt/_EVT_VARIANT"]
old-location: wes\evt_variant.htm
tech.root: wes
ms.assetid: 4b0f338b-0b66-4ba5-9e29-b15afe15a2d3
ms.date: 12/05/2018
ms.keywords: '*PEVT_VARIANT, EVT_VARIANT, EVT_VARIANT structure [EventLog], PEVT_VARIANT, PEVT_VARIANT structure pointer [EventLog], wes.evt_variant, winevt/PEVT_VARIANT, winevt/_EVT_VARIANT'
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
req.typenames: EVT_VARIANT, *PEVT_VARIANT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVT_VARIANT
 - winevt/_EVT_VARIANT
 - PEVT_VARIANT
 - winevt/PEVT_VARIANT
 - EVT_VARIANT
 - winevt/EVT_VARIANT
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
 - EVT_VARIANT
---

# EVT_VARIANT structure


## -description

Contains  event data or property values.

## -struct-fields

### -field BooleanVal

A Boolean value.

### -field SByteVal

A signed 8-bit integer value.

### -field Int16Val

A signed 16-bit integer value.

### -field Int32Val

A signed 32-bit integer value.

### -field Int64Val

A signed 64-bit integer value.

### -field ByteVal

An unsigned 8-bit integer value.

### -field UInt16Val

An unsigned 16-bit integer value.

### -field UInt32Val

An unsigned 32-bit integer value.

### -field UInt64Val

An unsigned 64-bit integer value.

### -field SingleVal

A single precision real value.

### -field DoubleVal

A double precision real value.

### -field FileTimeVal

An 8-byte FILETIME value.

### -field SysTimeVal

A SYSTEMTIME value.

### -field GuidVal

A 16-byte GUID value.

### -field StringVal

A null-terminated Unicode string.

### -field AnsiStringVal

A null-terminated ANSI string value.

### -field BinaryVal

A pointer to a hexadecimal binary value.

### -field SidVal

A 4-byte ASCII value. A security identifier (<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>) structure that uniquely identifies a user or group.

### -field SizeTVal

A pointer address. The size of the address (4 bytes or 8 bytes) depends on whether the provider ran on a 32-bit or 64-bit operating system.

### -field BooleanArr

A pointer to an array of Boolean values.

### -field SByteArr

A pointer to an array of signed 8-bit values.

### -field Int16Arr

A  pointer to an array of signed 16-bit values.

### -field Int32Arr

A pointer to an array of signed 32-bit values.

### -field Int64Arr

A pointer to an array of signed 64-bit values.

### -field ByteArr

A pointer to an array of unsigned 8-bit values.

### -field UInt16Arr

A pointer to an array of unsigned 16-bit values.

### -field UInt32Arr

A pointer to an array of unsigned 32-bit values.

### -field UInt64Arr

A pointer to an array of unsigned 64-bit values.

### -field SingleArr

A pointer to an array of single precision real values.

### -field DoubleArr

A pointer to an array of double precision real values.

### -field FileTimeArr

A pointer to an array of FILETIME values.

### -field SysTimeArr

A pointer to an array of SYSTEMTIME values.

### -field GuidArr

A pointer to an array of GUID values.

### -field StringArr

A pointer to an array of null-terminated Unicode strings.

### -field AnsiStringArr

A pointer to an array of null-terminated ANSI strings.

### -field SidArr

A pointer to an array of  4-byte ASCII values.

### -field SizeTArr

A pointer to an array of size_t values.

### -field EvtHandleVal

An  EVT_HANDLE value.

### -field XmlVal

An XML string value.

### -field XmlValArr

A pointer to an array of XML string values.

### -field Count

The number of elements in the array of values. Use <b>Count</b> if the <b>Type</b> member has the <b>EVT_VARIANT_TYPE_ARRAY</b> flag set.

### -field Type

A flag that specifies the data type of the variant. For possible values, see the <a href="/windows/desktop/api/winevt/ne-winevt-evt_variant_type">EVT_VARIANT_TYPE</a> enumeration.

The variant contains an array of values, if the <b>EVT_VARIANT_TYPE_ARRAY</b> flag is set. The members that end in "Arr" contain arrays of values. For example, you would use the <b>StringArr</b> member to access the variant data if the type is EvtVarTypeString and the <b>EVT_VARIANT_TYPE_ARRAY</b> flag is set.

You can use the <a href="/windows/desktop/WES/windows-event-log-constants">EVT_VARIANT_TYPE_MASK</a> constant to mask out the array bit to determine the variant's type.

## -see-also

<a href="/windows/desktop/api/winevt/ne-winevt-evt_system_property_id">EVT_SYSTEM_PROPERTY_ID</a>



<a href="/windows/desktop/api/winevt/ne-winevt-evt_variant_type">EVT_VARIANT_TYPE</a>



<a href="/windows/desktop/WES/windows-event-log-constants">EVT_VARIANT_TYPE_MASK</a>