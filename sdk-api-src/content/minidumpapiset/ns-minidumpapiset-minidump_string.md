---
UID: NS:minidumpapiset._MINIDUMP_STRING
title: MINIDUMP_STRING (minidumpapiset.h)
description: Describes a string.
helpviewer_keywords: ["*PMINIDUMP_STRING","MINIDUMP_STRING","MINIDUMP_STRING structure","PMINIDUMP_STRING","PMINIDUMP_STRING structure pointer","_MINIDUMP_STRING","_win32_minidump_string_str","base.minidump_string_str","minidumpapiset/MINIDUMP_STRING","minidumpapiset/PMINIDUMP_STRING"]
old-location: base\minidump_string_str.htm
tech.root: Debug
ms.assetid: b90b2b29-9d39-4a73-b5fb-bb6e04c94811
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_STRING, MINIDUMP_STRING, MINIDUMP_STRING structure, PMINIDUMP_STRING, PMINIDUMP_STRING structure pointer, _MINIDUMP_STRING, _win32_minidump_string_str, base.minidump_string_str, minidumpapiset/MINIDUMP_STRING, minidumpapiset/PMINIDUMP_STRING'
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
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
req.typenames: MINIDUMP_STRING, *PMINIDUMP_STRING
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_STRING
 - minidumpapiset/_MINIDUMP_STRING
 - PMINIDUMP_STRING
 - minidumpapiset/PMINIDUMP_STRING
 - MINIDUMP_STRING
 - minidumpapiset/MINIDUMP_STRING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_STRING
---

# MINIDUMP_STRING structure


## -description

Describes a string.

## -struct-fields

### -field Length

The size of the string in the <b>Buffer</b> member, in bytes. This size does not include the null-terminating character.

### -field Buffer

The null-terminated string.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_descriptor">MINIDUMP_HANDLE_DESCRIPTOR</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_module">MINIDUMP_MODULE</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_unloaded_module">MINIDUMP_UNLOADED_MODULE</a>