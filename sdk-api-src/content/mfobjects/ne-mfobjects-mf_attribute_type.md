---
UID: NE:mfobjects._MF_ATTRIBUTE_TYPE
title: MF_ATTRIBUTE_TYPE (mfobjects.h)
description: Defines the data type for a key/value pair.
helpviewer_keywords: ["1844fbe2-0a07-4c0c-9ffe-4c59fc01f793","MF_ATTRIBUTE_BLOB","MF_ATTRIBUTE_DOUBLE","MF_ATTRIBUTE_GUID","MF_ATTRIBUTE_IUNKNOWN","MF_ATTRIBUTE_STRING","MF_ATTRIBUTE_TYPE","MF_ATTRIBUTE_TYPE enumeration [Media Foundation]","MF_ATTRIBUTE_UINT32","MF_ATTRIBUTE_UINT64","mf.mf_attribute_type","mfobjects/MF_ATTRIBUTE_BLOB","mfobjects/MF_ATTRIBUTE_DOUBLE","mfobjects/MF_ATTRIBUTE_GUID","mfobjects/MF_ATTRIBUTE_IUNKNOWN","mfobjects/MF_ATTRIBUTE_STRING","mfobjects/MF_ATTRIBUTE_TYPE","mfobjects/MF_ATTRIBUTE_UINT32","mfobjects/MF_ATTRIBUTE_UINT64"]
old-location: mf\mf_attribute_type.htm
tech.root: mf
ms.assetid: 1844fbe2-0a07-4c0c-9ffe-4c59fc01f793
ms.date: 12/05/2018
ms.keywords: 1844fbe2-0a07-4c0c-9ffe-4c59fc01f793, MF_ATTRIBUTE_BLOB, MF_ATTRIBUTE_DOUBLE, MF_ATTRIBUTE_GUID, MF_ATTRIBUTE_IUNKNOWN, MF_ATTRIBUTE_STRING, MF_ATTRIBUTE_TYPE, MF_ATTRIBUTE_TYPE enumeration [Media Foundation], MF_ATTRIBUTE_UINT32, MF_ATTRIBUTE_UINT64, mf.mf_attribute_type, mfobjects/MF_ATTRIBUTE_BLOB, mfobjects/MF_ATTRIBUTE_DOUBLE, mfobjects/MF_ATTRIBUTE_GUID, mfobjects/MF_ATTRIBUTE_IUNKNOWN, mfobjects/MF_ATTRIBUTE_STRING, mfobjects/MF_ATTRIBUTE_TYPE, mfobjects/MF_ATTRIBUTE_UINT32, mfobjects/MF_ATTRIBUTE_UINT64
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MF_ATTRIBUTE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_ATTRIBUTE_TYPE
 - mfobjects/_MF_ATTRIBUTE_TYPE
 - MF_ATTRIBUTE_TYPE
 - mfobjects/MF_ATTRIBUTE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MF_ATTRIBUTE_TYPE
---

# MF_ATTRIBUTE_TYPE enumeration


## -description

Defines the data type for a key/value pair.

## -enum-fields

### -field MF_ATTRIBUTE_UINT32:VT_UI4

Unsigned 32-bit integer.

### -field MF_ATTRIBUTE_UINT64:VT_UI8

Unsigned 64-bit integer.

### -field MF_ATTRIBUTE_DOUBLE:VT_R8

Floating-point number.

### -field MF_ATTRIBUTE_GUID:VT_CLSID

<b>GUID</b> value.

### -field MF_ATTRIBUTE_STRING:VT_LPWSTR

NULL-terminated wide-character string.

### -field MF_ATTRIBUTE_BLOB

Byte array.

### -field MF_ATTRIBUTE_IUNKNOWN:VT_UNKNOWN

<b>IUnknown</b> pointer.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
