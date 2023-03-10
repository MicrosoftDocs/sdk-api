---
UID: NE:mi._MI_Type
title: MI_Type (mi.h)
description: These values specify the data type of qualifiers, properties, references, parameters, and method return values for the CIM data types.
helpviewer_keywords: ["MI_ARRAY","MI_BOOLEAN","MI_BOOLEANA","MI_CHAR16","MI_CHAR16A","MI_DATETIME","MI_DATETIMEA","MI_INSTANCE","MI_INSTANCEA","MI_REAL32","MI_REAL32A","MI_REAL64","MI_REAL64A","MI_REFERENCE","MI_REFERENCEA","MI_SINT16","MI_SINT16A","MI_SINT32","MI_SINT32A","MI_SINT64","MI_SINT64A","MI_SINT8","MI_SINT8A","MI_STRING","MI_STRINGA","MI_Type","MI_Type enumeration [Windows Management Infrastructure (MI)]","MI_UINT16","MI_UINT16A","MI_UINT32","MI_UINT32A","MI_UINT64","MI_UINT64A","MI_UINT8","MI_UINT8A","mi/MI_ARRAY","mi/MI_BOOLEAN","mi/MI_BOOLEANA","mi/MI_CHAR16","mi/MI_CHAR16A","mi/MI_DATETIME","mi/MI_DATETIMEA","mi/MI_INSTANCE","mi/MI_INSTANCEA","mi/MI_REAL32","mi/MI_REAL32A","mi/MI_REAL64","mi/MI_REAL64A","mi/MI_REFERENCE","mi/MI_REFERENCEA","mi/MI_SINT16","mi/MI_SINT16A","mi/MI_SINT32","mi/MI_SINT32A","mi/MI_SINT64","mi/MI_SINT64A","mi/MI_SINT8","mi/MI_SINT8A","mi/MI_STRING","mi/MI_STRINGA","mi/MI_Type","mi/MI_UINT16","mi/MI_UINT16A","mi/MI_UINT32","mi/MI_UINT32A","mi/MI_UINT64","mi/MI_UINT64A","mi/MI_UINT8","mi/MI_UINT8A","wmi._mi_type","wmi_v2.mi_type"]
old-location: wmi_v2\mi_type.htm
tech.root: wmi_v2
ms.assetid: 21015eb7-9630-458e-acd8-923ee86ac2b8
ms.date: 12/05/2018
ms.keywords: MI_ARRAY, MI_BOOLEAN, MI_BOOLEANA, MI_CHAR16, MI_CHAR16A, MI_DATETIME, MI_DATETIMEA, MI_INSTANCE, MI_INSTANCEA, MI_REAL32, MI_REAL32A, MI_REAL64, MI_REAL64A, MI_REFERENCE, MI_REFERENCEA, MI_SINT16, MI_SINT16A, MI_SINT32, MI_SINT32A, MI_SINT64, MI_SINT64A, MI_SINT8, MI_SINT8A, MI_STRING, MI_STRINGA, MI_Type, MI_Type enumeration [Windows Management Infrastructure (MI)], MI_UINT16, MI_UINT16A, MI_UINT32, MI_UINT32A, MI_UINT64, MI_UINT64A, MI_UINT8, MI_UINT8A, mi/MI_ARRAY, mi/MI_BOOLEAN, mi/MI_BOOLEANA, mi/MI_CHAR16, mi/MI_CHAR16A, mi/MI_DATETIME, mi/MI_DATETIMEA, mi/MI_INSTANCE, mi/MI_INSTANCEA, mi/MI_REAL32, mi/MI_REAL32A, mi/MI_REAL64, mi/MI_REAL64A, mi/MI_REFERENCE, mi/MI_REFERENCEA, mi/MI_SINT16, mi/MI_SINT16A, mi/MI_SINT32, mi/MI_SINT32A, mi/MI_SINT64, mi/MI_SINT64A, mi/MI_SINT8, mi/MI_SINT8A, mi/MI_STRING, mi/MI_STRINGA, mi/MI_Type, mi/MI_UINT16, mi/MI_UINT16A, mi/MI_UINT32, mi/MI_UINT32A, mi/MI_UINT64, mi/MI_UINT64A, mi/MI_UINT8, mi/MI_UINT8A, wmi._mi_type, wmi_v2.mi_type
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_Type
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_Type
 - mi/_MI_Type
 - MI_Type
 - mi/MI_Type
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Type
---

# MI_Type enumeration


## -description

These
values specify the data type of qualifiers, properties, references,
parameters, and method return values for the CIM data types.

## -enum-fields

### -field MI_BOOLEAN:0

unsigned char

### -field MI_UINT8:1

unsigned char

### -field MI_SINT8:2

signed char

### -field MI_UINT16:3

unsigned short

### -field MI_SINT16:4

signed short

### -field MI_UINT32:5

unsigned int

### -field MI_SINT32:6

signed int

### -field MI_UINT64:7

unsigned __int64

### -field MI_SINT64:8

signed __int64

### -field MI_REAL32:9

float

### -field MI_REAL64:10

double

### -field MI_CHAR16:11

unsigned short

### -field MI_DATETIME:12

Structure holding a union of <a href="/windows/desktop/api/mi/ns-mi-mi_timestamp">MI_Timestamp</a> or <a href="/windows/desktop/api/mi/ns-mi-mi_interval">MI_Interval</a>.

### -field MI_STRING:13

MI_CHAR*

### -field MI_REFERENCE:14

This is encoded as an <a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a>, but usually only the key properties are set.

### -field MI_INSTANCE:15

### -field MI_BOOLEANA:16

Array of <b>MI_BOOLEAN</b> types.

### -field MI_UINT8A:17

Array of <b>MI_UINT8</b> types.

### -field MI_SINT8A:18

Array of <b>MI_SINT8</b> types.

### -field MI_UINT16A:19

Array of <b>MI_UINT16</b> types.

### -field MI_SINT16A:20

Array of <b>MI_SINT16</b> types.

### -field MI_UINT32A:21

Array of <b>MI_UINT32</b> types.

### -field MI_SINT32A:22

Array of <b>MI_SINT32</b> types.

### -field MI_UINT64A:23

Array of <b>MI_UINT64</b> types.

### -field MI_SINT64A:24

Array of <b>MI_SINT64</b> types.

### -field MI_REAL32A:25

Array of <b>MI_REAL32</b> types.

### -field MI_REAL64A:26

Array of <b>MI_REAL64</b> types.

### -field MI_CHAR16A:27

Array of <b>MI_CHAR16</b> types.

### -field MI_DATETIMEA:28

Array of <b>MI_DATETIME</b> structures.

### -field MI_STRINGA:29

Array of <b>MI_STRING</b> types.

### -field MI_REFERENCEA:30

Array of <b>MI_REFERENCE</b> types.

### -field MI_INSTANCEA:31

Array of <b>MI_INSTANCE</b> types.

### -field MI_ARRAY:16

MI_ARRAY is not an actual type, rather this is the bit that signifies  the type is an array.
