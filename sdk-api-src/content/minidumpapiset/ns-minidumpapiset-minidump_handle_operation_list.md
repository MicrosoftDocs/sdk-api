---
UID: NS:minidumpapiset._MINIDUMP_HANDLE_OPERATION_LIST
title: MINIDUMP_HANDLE_OPERATION_LIST (minidumpapiset.h)
description: Contains a list of handle operations.
helpviewer_keywords: ["*PMINIDUMP_HANDLE_OPERATION_LIST","MINIDUMP_HANDLE_OPERATION_LIST","MINIDUMP_HANDLE_OPERATION_LIST structure","PMINIDUMP_HANDLE_OPERATION_LIST","PMINIDUMP_HANDLE_OPERATION_LIST structure pointer","_MINIDUMP_HANDLE_OPERATION_LISTa","base.minidump_handle_operation_list","minidumpapiset/MINIDUMP_HANDLE_OPERATION_LIST","minidumpapiset/PMINIDUMP_HANDLE_OPERATION_LIST"]
old-location: base\minidump_handle_operation_list.htm
tech.root: Debug
ms.assetid: f7666ff5-a1ae-4ffb-b4ee-9fe5bb58fd36
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_HANDLE_OPERATION_LIST, MINIDUMP_HANDLE_OPERATION_LIST, MINIDUMP_HANDLE_OPERATION_LIST structure, PMINIDUMP_HANDLE_OPERATION_LIST, PMINIDUMP_HANDLE_OPERATION_LIST structure pointer, _MINIDUMP_HANDLE_OPERATION_LISTa, base.minidump_handle_operation_list, minidumpapiset/MINIDUMP_HANDLE_OPERATION_LIST, minidumpapiset/PMINIDUMP_HANDLE_OPERATION_LIST'
req.header: minidumpapiset.h
req.include-header: Dbghelp.h
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
req.typenames: MINIDUMP_HANDLE_OPERATION_LIST, *PMINIDUMP_HANDLE_OPERATION_LIST
req.redist: DbgHelp.dll 6.5 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_HANDLE_OPERATION_LIST
 - minidumpapiset/_MINIDUMP_HANDLE_OPERATION_LIST
 - PMINIDUMP_HANDLE_OPERATION_LIST
 - minidumpapiset/PMINIDUMP_HANDLE_OPERATION_LIST
 - MINIDUMP_HANDLE_OPERATION_LIST
 - minidumpapiset/MINIDUMP_HANDLE_OPERATION_LIST
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
 - MINIDUMP_HANDLE_OPERATION_LIST
---

# MINIDUMP_HANDLE_OPERATION_LIST structure


## -description

Contains a list of handle operations.

## -struct-fields

### -field SizeOfHeader

The size of the header data for the stream, in bytes. This is generally <code>sizeof(MINIDUMP_HANDLE_OPERATION_LIST)</code>.

### -field SizeOfEntry

The size of each entry following the header, in bytes. This is generally <code>sizeof(AVRF_HANDLE_OPERATION)</code>.

### -field NumberOfEntries

The number of entries in the stream.  These are generally <b>AVRF_HANDLE_OPERATION</b> structures. The entries follow the header.

### -field Reserved

This member is reserved for future use.

## -remarks

For a definition of the <b>AVRF_HANDLE_OPERATION</b> structure, see the Avrfsdk.h header file.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>