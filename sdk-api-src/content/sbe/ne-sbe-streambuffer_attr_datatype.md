---
UID: NE:sbe.STREAMBUFFER_ATTR_DATATYPE
title: STREAMBUFFER_ATTR_DATATYPE (sbe.h)
description: This topic applies only to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["STREAMBUFFER_ATTR_DATATYPE","STREAMBUFFER_ATTR_DATATYPE","STREAMBUFFER_ATTR_DATATYPE enumeration [Microsoft TV Technologies]","STREAMBUFFER_ATTR_DATATYPEEnumeration","STREAMBUFFER_TYPE_BINARY","STREAMBUFFER_TYPE_BOOL","STREAMBUFFER_TYPE_DWORD","STREAMBUFFER_TYPE_GUID","STREAMBUFFER_TYPE_QWORD","STREAMBUFFER_TYPE_STRING","STREAMBUFFER_TYPE_WORD","mstv.streambuffer_attr_datatype","sbe/STREAMBUFFER_ATTR_DATATYPE","sbe/STREAMBUFFER_TYPE_BINARY","sbe/STREAMBUFFER_TYPE_BOOL","sbe/STREAMBUFFER_TYPE_DWORD","sbe/STREAMBUFFER_TYPE_GUID","sbe/STREAMBUFFER_TYPE_QWORD","sbe/STREAMBUFFER_TYPE_STRING","sbe/STREAMBUFFER_TYPE_WORD"]
old-location: mstv\streambuffer_attr_datatype.htm
tech.root: mstv
ms.assetid: be478769-d9ac-4e42-b5f6-94b5656e2596
ms.date: 12/05/2018
ms.keywords: STREAMBUFFER_ATTR_DATATYPE, STREAMBUFFER_ATTR_DATATYPE , STREAMBUFFER_ATTR_DATATYPE enumeration [Microsoft TV Technologies], STREAMBUFFER_ATTR_DATATYPEEnumeration, STREAMBUFFER_TYPE_BINARY, STREAMBUFFER_TYPE_BOOL, STREAMBUFFER_TYPE_DWORD, STREAMBUFFER_TYPE_GUID, STREAMBUFFER_TYPE_QWORD, STREAMBUFFER_TYPE_STRING, STREAMBUFFER_TYPE_WORD, mstv.streambuffer_attr_datatype, sbe/STREAMBUFFER_ATTR_DATATYPE, sbe/STREAMBUFFER_TYPE_BINARY, sbe/STREAMBUFFER_TYPE_BOOL, sbe/STREAMBUFFER_TYPE_DWORD, sbe/STREAMBUFFER_TYPE_GUID, sbe/STREAMBUFFER_TYPE_QWORD, sbe/STREAMBUFFER_TYPE_STRING, sbe/STREAMBUFFER_TYPE_WORD
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: STREAMBUFFER_ATTR_DATATYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - STREAMBUFFER_ATTR_DATATYPE
 - sbe/STREAMBUFFER_ATTR_DATATYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sbe.h
api_name:
 - STREAMBUFFER_ATTR_DATATYPE
---

# STREAMBUFFER_ATTR_DATATYPE enumeration


## -description

This topic applies only to Windows XP Service Pack 1 or later.
        



The <b>STREAMBUFFER_ATTR_DATATYPE</b> enumeration defines the data type for an attribute.

## -enum-fields

### -field STREAMBUFFER_TYPE_DWORD:0

The attribute is a 32-bit <b>DWORD</b> value.

### -field STREAMBUFFER_TYPE_STRING:1

The attribute is a null-terminated wide-character string.

### -field STREAMBUFFER_TYPE_BINARY:2

The attribute is an array of bytes.

### -field STREAMBUFFER_TYPE_BOOL:3

The attribute is a 32-bit Boolean value.

### -field STREAMBUFFER_TYPE_QWORD:4

The attribute is a 64-bit <b>QWORD</b> value.

### -field STREAMBUFFER_TYPE_WORD:5

The attribute is a 16-bit <b>WORD</b> value.

### -field STREAMBUFFER_TYPE_GUID:6

The attribute is a 128-bit <b>GUID</b> value.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferrecordingattribute">IStreamBufferRecordingAttribute Interface</a>



<a href="/previous-versions/windows/desktop/api/sbe/ns-sbe-streambuffer_attribute">STREAMBUFFER_ATTRIBUTE Structure</a>



<a href="/previous-versions/windows/desktop/mstv/stream-buffer-engine-types">Stream Buffer Engine Enumeration Types</a>
