---
UID: NE:wbemcli.tag_CIMTYPE_ENUMERATION
title: CIMTYPE_ENUMERATION (wbemcli.h)
description: Defines values that specify different CIM data types.
helpviewer_keywords: ["CIMTYPE_ENUMERATION","CIMTYPE_ENUMERATION enumeration [Windows Management Instrumentation]","CIM_BOOLEAN","CIM_CHAR16","CIM_DATETIME","CIM_EMPTY","CIM_FLAG_ARRAY","CIM_ILLEGAL","CIM_OBJECT","CIM_REAL32","CIM_REAL64","CIM_REFERENCE","CIM_SINT16","CIM_SINT32","CIM_SINT64","CIM_SINT8","CIM_STRING","CIM_UINT16","CIM_UINT32","CIM_UINT64","CIM_UINT8","wbemcli/CIMTYPE_ENUMERATION","wbemcli/CIM_BOOLEAN","wbemcli/CIM_CHAR16","wbemcli/CIM_DATETIME","wbemcli/CIM_EMPTY","wbemcli/CIM_FLAG_ARRAY","wbemcli/CIM_ILLEGAL","wbemcli/CIM_OBJECT","wbemcli/CIM_REAL32","wbemcli/CIM_REAL64","wbemcli/CIM_REFERENCE","wbemcli/CIM_SINT16","wbemcli/CIM_SINT32","wbemcli/CIM_SINT64","wbemcli/CIM_SINT8","wbemcli/CIM_STRING","wbemcli/CIM_UINT16","wbemcli/CIM_UINT32","wbemcli/CIM_UINT64","wbemcli/CIM_UINT8","wmi.cimtype_enumeration"]
old-location: wmi\cimtype_enumeration.htm
tech.root: wmi
ms.assetid: ab67954c-ead2-4906-9680-503612d3f12d
ms.date: 12/05/2018
ms.keywords: CIMTYPE_ENUMERATION, CIMTYPE_ENUMERATION enumeration [Windows Management Instrumentation], CIM_BOOLEAN, CIM_CHAR16, CIM_DATETIME, CIM_EMPTY, CIM_FLAG_ARRAY, CIM_ILLEGAL, CIM_OBJECT, CIM_REAL32, CIM_REAL64, CIM_REFERENCE, CIM_SINT16, CIM_SINT32, CIM_SINT64, CIM_SINT8, CIM_STRING, CIM_UINT16, CIM_UINT32, CIM_UINT64, CIM_UINT8, wbemcli/CIMTYPE_ENUMERATION, wbemcli/CIM_BOOLEAN, wbemcli/CIM_CHAR16, wbemcli/CIM_DATETIME, wbemcli/CIM_EMPTY, wbemcli/CIM_FLAG_ARRAY, wbemcli/CIM_ILLEGAL, wbemcli/CIM_OBJECT, wbemcli/CIM_REAL32, wbemcli/CIM_REAL64, wbemcli/CIM_REFERENCE, wbemcli/CIM_SINT16, wbemcli/CIM_SINT32, wbemcli/CIM_SINT64, wbemcli/CIM_SINT8, wbemcli/CIM_STRING, wbemcli/CIM_UINT16, wbemcli/CIM_UINT32, wbemcli/CIM_UINT64, wbemcli/CIM_UINT8, wmi.cimtype_enumeration
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: CIMTYPE_ENUMERATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_CIMTYPE_ENUMERATION
 - wbemcli/tag_CIMTYPE_ENUMERATION
 - CIMTYPE_ENUMERATION
 - wbemcli/CIMTYPE_ENUMERATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - CIMTYPE_ENUMERATION
---

# CIMTYPE_ENUMERATION enumeration


## -description

The <b>CIMTYPE_ENUMERATION</b> enumeration defines values that specify different CIM data types. All the values in the enumeration are types defined by the Distributed Management Task Force (DMTF). For more information about the DMTF and the CIM data types, see <a href="https://www.dmtf.org/standards/cim">http://www.dmtf.org/standards/cim/cim_spec_v22</a>.

## -enum-fields

### -field CIM_ILLEGAL:0xfff

An illegal value.

### -field CIM_EMPTY:0

An empty (null) value.

### -field CIM_SINT8:16

An 8-bit signed integer.

### -field CIM_UINT8:17

An 8-bit unsigned integer.

### -field CIM_SINT16:2

A 16-bit signed integer.

### -field CIM_UINT16:18

A 16-bit unsigned integer.

### -field CIM_SINT32:3

A 32-bit signed integer.

### -field CIM_UINT32:19

A 32-bit unsigned integer.

### -field CIM_SINT64:20

A 64-bit signed integer.

### -field CIM_UINT64:21

A 64-bit unsigned integer.

### -field CIM_REAL32:4

A 32-bit real number.

### -field CIM_REAL64:5

A 64-bit real number.

### -field CIM_BOOLEAN:11

A Boolean value.

### -field CIM_STRING:8

A string value.

### -field CIM_DATETIME:101

A DateTime value.

### -field CIM_REFERENCE:102

Reference (__Path) of another Object.

### -field CIM_CHAR16:103

A 16-bit character value.

### -field CIM_OBJECT:13

An Object value.

### -field CIM_FLAG_ARRAY:0x2000

An array value.

