---
UID: NE:minidumpapiset._MINIDUMP_STREAM_TYPE
title: MINIDUMP_STREAM_TYPE (minidumpapiset.h)
description: Represents the type of a minidump data stream.
helpviewer_keywords: ["CommentStreamA","CommentStreamW","ExceptionStream","FunctionTableStream","HandleDataStream","HandleOperationListStream","LastReservedStream","MINIDUMP_STREAM_TYPE","MINIDUMP_STREAM_TYPE enumeration","Memory64ListStream","MemoryInfoListStream","MemoryListStream","MiscInfoStream","ModuleListStream","ReservedStream0","ReservedStream1","SystemInfoStream","ThreadExListStream","ThreadInfoListStream","ThreadListStream","UnloadedModuleListStream","UnusedStream","_win32_minidump_stream_type","base.minidump_stream_type","minidumpapiset/CommentStreamA","minidumpapiset/CommentStreamW","minidumpapiset/ExceptionStream","minidumpapiset/FunctionTableStream","minidumpapiset/HandleDataStream","minidumpapiset/HandleOperationListStream","minidumpapiset/LastReservedStream","minidumpapiset/MINIDUMP_STREAM_TYPE","minidumpapiset/Memory64ListStream","minidumpapiset/MemoryInfoListStream","minidumpapiset/MemoryListStream","minidumpapiset/MiscInfoStream","minidumpapiset/ModuleListStream","minidumpapiset/ReservedStream0","minidumpapiset/ReservedStream1","minidumpapiset/SystemInfoStream","minidumpapiset/ThreadExListStream","minidumpapiset/ThreadInfoListStream","minidumpapiset/ThreadListStream","minidumpapiset/UnloadedModuleListStream","minidumpapiset/UnusedStream"]
old-location: base\minidump_stream_type.htm
tech.root: Debug
ms.assetid: 495136a0-2fed-47ca-8233-7e813b43b82f
ms.date: 12/05/2018
ms.keywords: CommentStreamA, CommentStreamW, ExceptionStream, FunctionTableStream, HandleDataStream, HandleOperationListStream, LastReservedStream, MINIDUMP_STREAM_TYPE, MINIDUMP_STREAM_TYPE enumeration, Memory64ListStream, MemoryInfoListStream, MemoryListStream, MiscInfoStream, ModuleListStream, ReservedStream0, ReservedStream1, SystemInfoStream, ThreadExListStream, ThreadInfoListStream, ThreadListStream, UnloadedModuleListStream, UnusedStream, _win32_minidump_stream_type, base.minidump_stream_type, minidumpapiset/CommentStreamA, minidumpapiset/CommentStreamW, minidumpapiset/ExceptionStream, minidumpapiset/FunctionTableStream, minidumpapiset/HandleDataStream, minidumpapiset/HandleOperationListStream, minidumpapiset/LastReservedStream, minidumpapiset/MINIDUMP_STREAM_TYPE, minidumpapiset/Memory64ListStream, minidumpapiset/MemoryInfoListStream, minidumpapiset/MemoryListStream, minidumpapiset/MiscInfoStream, minidumpapiset/ModuleListStream, minidumpapiset/ReservedStream0, minidumpapiset/ReservedStream1, minidumpapiset/SystemInfoStream, minidumpapiset/ThreadExListStream, minidumpapiset/ThreadInfoListStream, minidumpapiset/ThreadListStream, minidumpapiset/UnloadedModuleListStream, minidumpapiset/UnusedStream
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
req.typenames: MINIDUMP_STREAM_TYPE
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_STREAM_TYPE
 - minidumpapiset/_MINIDUMP_STREAM_TYPE
 - MINIDUMP_STREAM_TYPE
 - minidumpapiset/MINIDUMP_STREAM_TYPE
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
 - MINIDUMP_STREAM_TYPE
---

# MINIDUMP_STREAM_TYPE enumeration


## -description

Represents the type of a minidump data stream.

## -enum-fields

### -field UnusedStream:0

Reserved. Do not use this enumeration value.

### -field ReservedStream0:1

Reserved. Do not use this enumeration value.

### -field ReservedStream1:2

Reserved. Do not use this enumeration value.

### -field ThreadListStream:3

The stream contains thread information. For more information, see 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_thread_list">MINIDUMP_THREAD_LIST</a>.

### -field ModuleListStream:14

The stream contains module information. For more information, see 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_module_list">MINIDUMP_MODULE_LIST</a>.

### -field MemoryListStream:5

The stream contains memory allocation information. For more information, see 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_list">MINIDUMP_MEMORY_LIST</a>.

### -field ExceptionStream:6

The stream contains exception information. For more information, see 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_stream">MINIDUMP_EXCEPTION_STREAM</a>.

### -field SystemInfoStream:7

The stream contains general system information. For more information, see 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_system_info">MINIDUMP_SYSTEM_INFO</a>.

### -field ThreadExListStream:8

The stream contains extended thread information. For more information, see 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_ex_list">MINIDUMP_THREAD_EX_LIST</a>.

### -field Memory64ListStream:9

The stream contains memory allocation information. For more information, see 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory64_list">MINIDUMP_MEMORY64_LIST</a>.

### -field CommentStreamA:10

The stream contains an ANSI string used for documentation purposes.

### -field CommentStreamW:11

The stream contains a Unicode string used for documentation purposes.

### -field HandleDataStream:12

The stream contains high-level information about the active operating system handles. For more information, see 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_data_stream">MINIDUMP_HANDLE_DATA_STREAM</a>.

### -field FunctionTableStream:13

The stream contains function table information. For more information, see 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_function_table_stream">MINIDUMP_FUNCTION_TABLE_STREAM</a>.

### -field UnloadedModuleListStream:14

The stream contains module information for the unloaded modules. For more information, see 
<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_unloaded_module_list">MINIDUMP_UNLOADED_MODULE_LIST</a>.

<b>DbgHelp 5.1:  </b>This value is not supported.

### -field MiscInfoStream:15

The stream contains miscellaneous information. For more information, see 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_misc_info">MINIDUMP_MISC_INFO</a> or <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_misc_info_2">MINIDUMP_MISC_INFO_2</a>.

<b>DbgHelp 5.1:  </b>This value is not supported.

### -field MemoryInfoListStream:16

The stream contains memory region description information. It corresponds to the information that would be returned for the process from the <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_info_list">VirtualQuery</a> function. For more information, see <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_memory_info_list">MINIDUMP_MEMORY_INFO_LIST</a>.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field ThreadInfoListStream:17

The stream contains thread state information. For more information, see <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_info_list">MINIDUMP_THREAD_INFO_LIST</a>.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field HandleOperationListStream:18

This stream contains operation list information. For more information, see <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_operation_list">MINIDUMP_HANDLE_OPERATION_LIST</a>.

<b>DbgHelp 6.4 and earlier:  </b>This value is not supported.

### -field TokenStream:19

### -field JavaScriptDataStream:20

### -field SystemMemoryInfoStream:21

### -field ProcessVmCountersStream:22

### -field IptTraceStream:23

### -field ThreadNamesStream:24

### -field ceStreamNull:0x8000

### -field ceStreamSystemInfo:0x8001

### -field ceStreamException:0x8002

### -field ceStreamModuleList:0x8003

### -field ceStreamProcessList:0x8004

### -field ceStreamThreadList:0x8005

### -field ceStreamThreadContextList:0x8006

### -field ceStreamThreadCallStackList:0x8007

### -field ceStreamMemoryVirtualList:0x8008

### -field ceStreamMemoryPhysicalList:0x8009

### -field ceStreamBucketParameters:0x800A

### -field ceStreamProcessModuleMap:0x800B

### -field ceStreamDiagnosisList:0x800C

### -field LastReservedStream:0xffff

Any value greater than this value will not be used by the system and can be used to represent application-defined data streams. For more information, see 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_user_stream">MINIDUMP_USER_STREAM</a>.

## -remarks

In this context, a data stream is a set of data in a minidump file.

The <b>StreamType</b> member of the 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_directory">MINIDUMP_DIRECTORY</a> structure can be one of these types. Additional types may be added in the future, so if a program reading the minidump header encounters a stream type it does not recognize, it should ignore the stream altogether.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_directory">MINIDUMP_DIRECTORY</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_stream">MINIDUMP_EXCEPTION_STREAM</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_function_table_stream">MINIDUMP_FUNCTION_TABLE_STREAM</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_data_stream">MINIDUMP_HANDLE_DATA_STREAM</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_operation_list">MINIDUMP_HANDLE_OPERATION_LIST</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_info_list">MINIDUMP_MEMORY_INFO_LIST</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_list">MINIDUMP_MEMORY_LIST</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_misc_info">MINIDUMP_MISC_INFO</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_module_list">MINIDUMP_MODULE_LIST</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_system_info">MINIDUMP_SYSTEM_INFO</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_ex_list">MINIDUMP_THREAD_EX_LIST</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_info_list">MINIDUMP_THREAD_INFO_LIST</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_thread_list">MINIDUMP_THREAD_LIST</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_unloaded_module_list">MINIDUMP_UNLOADED_MODULE_LIST</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_user_stream">MINIDUMP_USER_STREAM</a>
