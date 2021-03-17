---
UID: NF:minidumpapiset.MiniDumpReadDumpStream
title: MiniDumpReadDumpStream function (minidumpapiset.h)
description: Reads a stream from a user-mode minidump file.
helpviewer_keywords: ["MiniDumpReadDumpStream","MiniDumpReadDumpStream function","_win32_minidumpreaddumpstream","base.minidumpreaddumpstream","minidumpapiset/MiniDumpReadDumpStream"]
old-location: base\minidumpreaddumpstream.htm
tech.root: Debug
ms.assetid: 56df69aa-55b6-451b-a003-3ee88dc934f9
ms.date: 12/05/2018
ms.keywords: MiniDumpReadDumpStream, MiniDumpReadDumpStream function, _win32_minidumpreaddumpstream, base.minidumpreaddumpstream, minidumpapiset/MiniDumpReadDumpStream
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll; Dbgcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll and Dbgcore.dll
ms.custom: 19H1
f1_keywords:
 - MiniDumpReadDumpStream
 - minidumpapiset/MiniDumpReadDumpStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
 - Dbgcore.dll
 - API-MS-Win-Core-Debug-MiniDump-L1-1-0.dll
 - DbgCore.dll
api_name:
 - MiniDumpReadDumpStream
---

# MiniDumpReadDumpStream function


## -description

Reads a stream from a user-mode minidump file.

## -parameters

### -param BaseOfDump [in]

A pointer to the base of the mapped minidump file. The file should have been mapped into memory using the 
      <a href="/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile">MapViewOfFile</a> function.

### -param StreamNumber [in]

The type of data to be read from the minidump file. This member can be one of the values in the 
      <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a> enumeration.

### -param Dir [out]

A pointer to a <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_directory">MINIDUMP_DIRECTORY</a> 
      structure.

### -param StreamPointer [out]

A pointer to the beginning of the minidump stream. The format of this stream depends on the value of 
      <i>StreamNumber</i>. For more information, see 
      <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>.

### -param StreamSize [out]

The size of the stream pointed to by <i>StreamPointer</i>, in bytes.

## -returns

If the function succeeds, the return value is <b>TRUE</b>; otherwise, the return 
       value is <b>FALSE</b>.

## -remarks

In this context, a data stream is a block of data written to a minidump file.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_directory">MINIDUMP_DIRECTORY</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>



<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>