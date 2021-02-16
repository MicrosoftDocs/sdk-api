---
UID: NS:ndattrib.tagHELPER_ATTRIBUTE
title: HELPER_ATTRIBUTE (ndattrib.h)
description: The HELPER_ATTRIBUTE structure contains all NDF supported data types.
helpviewer_keywords: ["*PHELPER_ATTRIBUTE","HELPER_ATTRIBUTE","HELPER_ATTRIBUTE structure [NDF]","ndattrib/HELPER_ATTRIBUTE","ndf.helper_attribute"]
old-location: ndf\helper_attribute.htm
tech.root: NDF
ms.assetid: bff9303e-7fab-49af-b213-aa0a9c83676e
ms.date: 12/05/2018
ms.keywords: '*PHELPER_ATTRIBUTE, HELPER_ATTRIBUTE, HELPER_ATTRIBUTE structure [NDF], ndattrib/HELPER_ATTRIBUTE, ndf.helper_attribute'
req.header: ndattrib.h
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
req.typenames: HELPER_ATTRIBUTE, *PHELPER_ATTRIBUTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHELPER_ATTRIBUTE
 - ndattrib/tagHELPER_ATTRIBUTE
 - PHELPER_ATTRIBUTE
 - ndattrib/PHELPER_ATTRIBUTE
 - HELPER_ATTRIBUTE
 - ndattrib/HELPER_ATTRIBUTE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndattrib.h
api_name:
 - HELPER_ATTRIBUTE
---

# HELPER_ATTRIBUTE structure


## -description

The <b>HELPER_ATTRIBUTE</b> structure contains all NDF supported data types.

## -struct-fields

### -field pwszName

Type: <b>[string] LPWSTR</b>

A pointer to a null-terminated string that contains the name of the attribute.

### -field type

Type: <b><a href="/windows/desktop/api/ndattrib/ne-ndattrib-attribute_type">ATTRIBUTE_TYPE</a></b>

The type of helper attribute.

### -field Boolean

Type: <b>BOOL</b>

A True or False value. Used when <b>type</b> is <b>AT_BOOLEAN</b>.

### -field Char

Type: <b>char</b>

A character value. Used when  <b>type</b> is <b>AT_INT8</b>.

### -field Byte

Type: <b>byte</b>

A byte value. Used when <b>type</b> is <b>AT_UINT8</b>.

### -field Short

Type: <b>short</b>

A 16-bit  signed value. Used when <b>type</b> is <b>AT_INT16</b>

### -field Word

Type: <b>WORD</b>

A 2-byte unsigned value. Used when <b>type</b> is <b>AT_UINT16</b>.

### -field Int

Type: <b>int</b>

A 4-byte signed value. Used when <b>type</b> is <b>AT_INT32</b>.

### -field DWord

Type: <b>DWORD</b>

A 4-byte unsigned value. Used when <b>type</b> is <b>AT_UINT32</b>.

### -field Int64

Type: <b>LONGLONG</b>

A 64-bit signed integer value. Used when <b>type</b> is <b>AT_INT64</b>.

### -field UInt64

Type: <b>ULONGLONG</b>

A 64-bit unsigned integer value. Used when <b>type</b> is <b>AT_UINT64</b>.

### -field PWStr

Type: <b>LPWSTR</b>

A null-terminated string value. Used when <b>type</b> is <b>AT_STRING</b>.

### -field Guid

Type: <b>GUID</b>

A GUID structure. Used when <b>type</b> is <b>AT_GUID</b>.

### -field LifeTime

Type: <b><a href="/windows/desktop/api/ndattrib/ns-ndattrib-life_time">LIFE_TIME</a></b>

A <a href="/windows/desktop/api/ndattrib/ns-ndattrib-life_time">LIFE_TIME</a> structure. Used when <b>type</b> is <b>AT_LIFE_TIME</b>.

### -field Address

Type: <b><a href="/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr">DIAG_SOCKADDR</a></b>

An IPv4 or IPv6 address. Used when <b>type</b> is <b>AT_SOCKADDR</b>.

### -field OctetString

Type: <b><a href="/windows/desktop/api/ndattrib/ns-ndattrib-octet_string">OCTET_STRING</a></b>

A byte array for undefined types. Used when <b>type</b> is <b>AT_OCTET_STRING</b>.

## -see-also

<a href="/windows/desktop/api/ndattrib/ne-ndattrib-attribute_type">ATTRIBUTE_TYPE</a>



<a href="/windows/desktop/NDF/copyhelperattribute">CopyHelperAttribute</a>



<a href="/windows/desktop/NDF/freehelperattributes">FreeHelperAttributes</a>