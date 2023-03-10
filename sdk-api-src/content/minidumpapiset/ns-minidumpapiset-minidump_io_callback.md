---
UID: NS:minidumpapiset._MINIDUMP_IO_CALLBACK
title: MINIDUMP_IO_CALLBACK (minidumpapiset.h)
description: Contains I/O callback information.
helpviewer_keywords: ["*PMINIDUMP_IO_CALLBACK","MINIDUMP_IO_CALLBACK","MINIDUMP_IO_CALLBACK structure","PMINIDUMP_IO_CALLBACK","PMINIDUMP_IO_CALLBACK structure pointer","_MINIDUMP_IO_CALLBACK","base.minidump_io_callback","minidumpapiset/MINIDUMP_IO_CALLBACK","minidumpapiset/PMINIDUMP_IO_CALLBACK"]
old-location: base\minidump_io_callback.htm
tech.root: Debug
ms.assetid: db38f035-1fb8-4715-846f-59392aac2d4e
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_IO_CALLBACK, MINIDUMP_IO_CALLBACK, MINIDUMP_IO_CALLBACK structure, PMINIDUMP_IO_CALLBACK, PMINIDUMP_IO_CALLBACK structure pointer, _MINIDUMP_IO_CALLBACK, base.minidump_io_callback, minidumpapiset/MINIDUMP_IO_CALLBACK, minidumpapiset/PMINIDUMP_IO_CALLBACK'
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
req.typenames: MINIDUMP_IO_CALLBACK, *PMINIDUMP_IO_CALLBACK
req.redist: DbgHelp.dll 6.5 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_IO_CALLBACK
 - minidumpapiset/_MINIDUMP_IO_CALLBACK
 - PMINIDUMP_IO_CALLBACK
 - minidumpapiset/PMINIDUMP_IO_CALLBACK
 - MINIDUMP_IO_CALLBACK
 - minidumpapiset/MINIDUMP_IO_CALLBACK
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
 - MINIDUMP_IO_CALLBACK
---

# MINIDUMP_IO_CALLBACK structure


## -description

Contains I/O callback information. This structure is used by the <a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a> function when the callback type is <b>IoStartCallback</b>, <b>IoWriteAllCallback</b>, or <b>IoFinishCallback</b>.

## -struct-fields

### -field Handle

The file handle passed to the <a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function.

### -field Offset

The offset for the write operation from the start of the minidump data. This member is used only with <b>IoWriteAllCallback</b>.

### -field Buffer

A pointer to a buffer that contains the data to be written. This member is used only with <b>IoWriteAllCallback</b>.

### -field BufferBytes

The size of the data buffer, in bytes. This member is used only with <b>IoWriteAllCallback</b>.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_input">MINIDUMP_CALLBACK_INPUT</a>



<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>