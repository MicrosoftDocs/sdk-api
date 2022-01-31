---
UID: NE:wmsdkidl.WMT_ATTR_DATATYPE
title: WMT_ATTR_DATATYPE (wmsdkidl.h)
description: The WMT_ATTR_DATATYPE enumeration defines the data type for a variably typed property.
helpviewer_keywords: ["WMT_ATTR_DATATYPE","WMT_ATTR_DATATYPE enumeration [windows Media Format]","WMT_TYPE_BINARY","WMT_TYPE_BOOL","WMT_TYPE_DWORD","WMT_TYPE_GUID","WMT_TYPE_QWORD","WMT_TYPE_STRING","WMT_TYPE_WORD","wmformat.wmt_attr_datatype","wmsdkidl/WMT_ATTR_DATATYPE","wmsdkidl/WMT_TYPE_BINARY","wmsdkidl/WMT_TYPE_BOOL","wmsdkidl/WMT_TYPE_DWORD","wmsdkidl/WMT_TYPE_GUID","wmsdkidl/WMT_TYPE_QWORD","wmsdkidl/WMT_TYPE_STRING","wmsdkidl/WMT_TYPE_WORD"]
old-location: wmformat\wmt_attr_datatype.htm
tech.root: wmformat
ms.assetid: 2a2756f9-2d76-48c9-bbea-35ee33a39918
ms.date: 12/05/2018
ms.keywords: WMT_ATTR_DATATYPE, WMT_ATTR_DATATYPE enumeration [windows Media Format], WMT_TYPE_BINARY, WMT_TYPE_BOOL, WMT_TYPE_DWORD, WMT_TYPE_GUID, WMT_TYPE_QWORD, WMT_TYPE_STRING, WMT_TYPE_WORD, wmformat.wmt_attr_datatype, wmsdkidl/WMT_ATTR_DATATYPE, wmsdkidl/WMT_TYPE_BINARY, wmsdkidl/WMT_TYPE_BOOL, wmsdkidl/WMT_TYPE_DWORD, wmsdkidl/WMT_TYPE_GUID, wmsdkidl/WMT_TYPE_QWORD, wmsdkidl/WMT_TYPE_STRING, wmsdkidl/WMT_TYPE_WORD
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WMT_ATTR_DATATYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMT_ATTR_DATATYPE
 - wmsdkidl/WMT_ATTR_DATATYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_ATTR_DATATYPE
---

# WMT_ATTR_DATATYPE enumeration


## -description

The <b>WMT_ATTR_DATATYPE</b> enumeration defines the data type for a variably typed property.

## -enum-fields

### -field WMT_TYPE_DWORD:0

The property is a 4-byte <b>DWORD</b> value.

### -field WMT_TYPE_STRING:1

The property is a null-terminated Unicode string.

### -field WMT_TYPE_BINARY:2

The property is an array of bytes.

### -field WMT_TYPE_BOOL:3

The property is a 4-byte Boolean value.

### -field WMT_TYPE_QWORD:4

The property is an 8-byte <b>QWORD</b> value.

### -field WMT_TYPE_WORD:5

The property is a 2-byte <b>WORD</b> value.

### -field WMT_TYPE_GUID:6

The property is a 128-bit (6-byte) GUID.

## -see-also

<a href="/windows/desktop/wmformat/attributes">Attributes</a>



<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
