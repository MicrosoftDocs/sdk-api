---
UID: NF:minidumpapiset.MiniDumpReadDumpStream
title: MiniDumpReadDumpStream function
author: windows-sdk-content
description: Reads a stream from a user-mode minidump file.
old-location: base\minidumpreaddumpstream.htm
tech.root: debug
ms.assetid: 56df69aa-55b6-451b-a003-3ee88dc934f9
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: MiniDumpReadDumpStream, MiniDumpReadDumpStream function, _win32_minidumpreaddumpstream, base.minidumpreaddumpstream, minidumpapiset/MiniDumpReadDumpStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll and Dbgcore.dll
---

# MiniDumpReadDumpStream function


## -description


Reads a stream from a user-mode minidump file.


## -parameters




### -param BaseOfDump [in]

A pointer to the base of the mapped minidump file. The file should have been mapped into memory using the 
      <a href="https://msdn.microsoft.com/df9f54cd-b2de-4107-a1c5-d5a07045851e">MapViewOfFile</a> function.


### -param StreamNumber [in]

The type of data to be read from the minidump file. This member can be one of the values in the 
      <a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a> enumeration.


### -param Dir [out]

A pointer to a <a href="https://msdn.microsoft.com/1262c218-5351-4fea-9d35-4654da7c5e44">MINIDUMP_DIRECTORY</a> 
      structure.


### -param StreamPointer [out]

A pointer to the beginning of the minidump stream. The format of this stream depends on the value of 
      <i>StreamNumber</i>. For more information, see 
      <a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>.


### -param StreamSize [out]

The size of the stream pointed to by <i>StreamPointer</i>, in bytes.


## -returns



If the function succeeds, the return value is <b>TRUE</b>; otherwise, the return 
       value is <b>FALSE</b>.




## -remarks



In this context, a data stream is a block of data written to a minidump file.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/1262c218-5351-4fea-9d35-4654da7c5e44">MINIDUMP_DIRECTORY</a>



<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>



<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a>
 

 

