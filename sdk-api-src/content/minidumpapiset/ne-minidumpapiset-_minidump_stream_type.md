---
UID: NE:minidumpapiset._MINIDUMP_STREAM_TYPE
title: "_MINIDUMP_STREAM_TYPE"
author: windows-sdk-content
description: Represents the type of a minidump data stream.
old-location: base\minidump_stream_type.htm
old-project: debug
ms.assetid: 495136a0-2fed-47ca-8233-7e813b43b82f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CommentStreamA, CommentStreamW, ExceptionStream, FunctionTableStream, HandleDataStream, HandleOperationListStream, LastReservedStream, MINIDUMP_STREAM_TYPE, MINIDUMP_STREAM_TYPE enumeration, Memory64ListStream, MemoryInfoListStream, MemoryListStream, MiscInfoStream, ModuleListStream, ReservedStream0, ReservedStream1, SystemInfoStream, ThreadExListStream, ThreadInfoListStream, ThreadListStream, UnloadedModuleListStream, UnusedStream, _MINIDUMP_STREAM_TYPE, _win32_minidump_stream_type, base.minidump_stream_type, minidumpapiset/CommentStreamA, minidumpapiset/CommentStreamW, minidumpapiset/ExceptionStream, minidumpapiset/FunctionTableStream, minidumpapiset/HandleDataStream, minidumpapiset/HandleOperationListStream, minidumpapiset/LastReservedStream, minidumpapiset/MINIDUMP_STREAM_TYPE, minidumpapiset/Memory64ListStream, minidumpapiset/MemoryInfoListStream, minidumpapiset/MemoryListStream, minidumpapiset/MiscInfoStream, minidumpapiset/ModuleListStream, minidumpapiset/ReservedStream0, minidumpapiset/ReservedStream1, minidumpapiset/SystemInfoStream, minidumpapiset/ThreadExListStream, minidumpapiset/ThreadInfoListStream, minidumpapiset/ThreadListStream, minidumpapiset/UnloadedModuleListStream, minidumpapiset/UnusedStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.redist: DbgHelp.dll 5.1 or later
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
tech.root: 
req.typenames: MINIDUMP_STREAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_STREAM_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_STREAM_TYPE enumeration


## -description


Represents the type of a minidump data stream.


## -enum-fields




### -field UnusedStream

Reserved. Do not use this enumeration value.


### -field ReservedStream0

Reserved. Do not use this enumeration value.


### -field ReservedStream1

Reserved. Do not use this enumeration value.


### -field ThreadListStream

The stream contains thread information. For more information, see 
<a href="https://msdn.microsoft.com/aa0491d3-e119-41d0-ab53-a108832745d0">MINIDUMP_THREAD_LIST</a>.


### -field ModuleListStream

The stream contains module information. For more information, see 
<a href="https://msdn.microsoft.com/9c30026d-9c72-472f-9d71-b15274459aae">MINIDUMP_MODULE_LIST</a>.


### -field MemoryListStream

The stream contains memory allocation information. For more information, see 
<a href="https://msdn.microsoft.com/83a38831-fb90-495c-9f5d-90971849a7a0">MINIDUMP_MEMORY_LIST</a>.


### -field ExceptionStream

The stream contains exception information. For more information, see 
<a href="https://msdn.microsoft.com/2de717dc-a9ac-4b81-9fab-992f22da9a0d">MINIDUMP_EXCEPTION_STREAM</a>.


### -field SystemInfoStream

The stream contains general system information. For more information, see 
<a href="https://msdn.microsoft.com/1d4e2a78-2184-4846-b51d-441bf1133ec0">MINIDUMP_SYSTEM_INFO</a>.


### -field ThreadExListStream

The stream contains extended thread information. For more information, see 
<a href="https://msdn.microsoft.com/653f1079-07c9-43b9-8dfe-05e99b365bdc">MINIDUMP_THREAD_EX_LIST</a>.


### -field Memory64ListStream

The stream contains memory allocation information. For more information, see 
<a href="https://msdn.microsoft.com/83a38831-fb90-495c-9f5d-90971849a7a0">MINIDUMP_MEMORY64_LIST</a>.


### -field CommentStreamA

The stream contains an ANSI string used for documentation purposes.


### -field CommentStreamW

The stream contains a Unicode string used for documentation purposes.


### -field HandleDataStream

The stream contains high-level information about the active operating system handles. For more information, see 
<a href="https://msdn.microsoft.com/5674df6b-77e0-4bca-8349-8217388902ed">MINIDUMP_HANDLE_DATA_STREAM</a>.


### -field FunctionTableStream

The stream contains function table information. For more information, see 
<a href="https://msdn.microsoft.com/b2845799-acc9-4410-9059-45f7a8313e9f">MINIDUMP_FUNCTION_TABLE_STREAM</a>.


### -field UnloadedModuleListStream

The stream contains module information for the unloaded modules. For more information, see 
<a href="https://msdn.microsoft.com/26a42ae7-f84d-451d-92e9-dbaffb15ca74">MINIDUMP_UNLOADED_MODULE_LIST</a>.

<b>DbgHelp 5.1:  </b>This value is not supported.


### -field MiscInfoStream

The stream contains miscellaneous information. For more information, see 
<a href="https://msdn.microsoft.com/c80bb631-b26b-40d4-ae35-1cf38ce45d51">MINIDUMP_MISC_INFO</a> or <a href="https://msdn.microsoft.com/34f46a51-9e41-4550-a080-1c7c7a603b54">MINIDUMP_MISC_INFO_2</a>.

<b>DbgHelp 5.1:  </b>This value is not supported.


### -field MemoryInfoListStream

The stream contains memory region description information. It corresponds to the information that would be returned for the process from the <a href="https://msdn.microsoft.com/3b1f7d27-1f5d-452e-b58f-560cd9b9cbd3">VirtualQuery</a> function. For more information, see <a href="https://msdn.microsoft.com/c1c9a79b-a35a-47e8-be4c-10b3c4ace937">MINIDUMP_MEMORY_INFO_LIST</a>.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.


### -field ThreadInfoListStream

The stream contains thread state information. For more information, see <a href="https://msdn.microsoft.com/ee02a8fa-c81d-4b23-b8a2-6ff31cdaf3de">MINIDUMP_THREAD_INFO_LIST</a>.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.


### -field HandleOperationListStream

This stream contains operation list information. For more information, see <a href="https://msdn.microsoft.com/f7666ff5-a1ae-4ffb-b4ee-9fe5bb58fd36">MINIDUMP_HANDLE_OPERATION_LIST</a>.

<b>DbgHelp 6.4 and earlier:  </b>This value is not supported.


### -field TokenStream


### -field JavaScriptDataStream


### -field SystemMemoryInfoStream


### -field ProcessVmCountersStream


### -field IptTraceStream


### -field ThreadNamesStream


### -field ceStreamNull


### -field ceStreamSystemInfo


### -field ceStreamException


### -field ceStreamModuleList


### -field ceStreamProcessList


### -field ceStreamThreadList


### -field ceStreamThreadContextList


### -field ceStreamThreadCallStackList


### -field ceStreamMemoryVirtualList


### -field ceStreamMemoryPhysicalList


### -field ceStreamBucketParameters


### -field ceStreamProcessModuleMap


### -field ceStreamDiagnosisList


### -field LastReservedStream

Any value greater than this value will not be used by the system and can be used to represent application-defined data streams. For more information, see 
<a href="https://msdn.microsoft.com/43eae98c-fba3-43a4-97e6-8b81874e856e">MINIDUMP_USER_STREAM</a>.


## -remarks



In this context, a data stream is a set of data in a minidump file.

The <b>StreamType</b> member of the 
<a href="https://msdn.microsoft.com/1262c218-5351-4fea-9d35-4654da7c5e44">MINIDUMP_DIRECTORY</a> structure can be one of these types. Additional types may be added in the future, so if a program reading the minidump header encounters a stream type it does not recognize, it should ignore the stream altogether.




## -see-also




<a href="https://msdn.microsoft.com/1262c218-5351-4fea-9d35-4654da7c5e44">MINIDUMP_DIRECTORY</a>



<a href="https://msdn.microsoft.com/2de717dc-a9ac-4b81-9fab-992f22da9a0d">MINIDUMP_EXCEPTION_STREAM</a>



<a href="https://msdn.microsoft.com/b2845799-acc9-4410-9059-45f7a8313e9f">MINIDUMP_FUNCTION_TABLE_STREAM</a>



<a href="https://msdn.microsoft.com/5674df6b-77e0-4bca-8349-8217388902ed">MINIDUMP_HANDLE_DATA_STREAM</a>



<a href="https://msdn.microsoft.com/f7666ff5-a1ae-4ffb-b4ee-9fe5bb58fd36">MINIDUMP_HANDLE_OPERATION_LIST</a>



<a href="https://msdn.microsoft.com/c1c9a79b-a35a-47e8-be4c-10b3c4ace937">MINIDUMP_MEMORY_INFO_LIST</a>



<a href="https://msdn.microsoft.com/83a38831-fb90-495c-9f5d-90971849a7a0">MINIDUMP_MEMORY_LIST</a>



<a href="https://msdn.microsoft.com/c80bb631-b26b-40d4-ae35-1cf38ce45d51">MINIDUMP_MISC_INFO</a>



<a href="https://msdn.microsoft.com/9c30026d-9c72-472f-9d71-b15274459aae">MINIDUMP_MODULE_LIST</a>



<a href="https://msdn.microsoft.com/1d4e2a78-2184-4846-b51d-441bf1133ec0">MINIDUMP_SYSTEM_INFO</a>



<a href="https://msdn.microsoft.com/653f1079-07c9-43b9-8dfe-05e99b365bdc">MINIDUMP_THREAD_EX_LIST</a>



<a href="https://msdn.microsoft.com/ee02a8fa-c81d-4b23-b8a2-6ff31cdaf3de">MINIDUMP_THREAD_INFO_LIST</a>



<a href="https://msdn.microsoft.com/aa0491d3-e119-41d0-ab53-a108832745d0">MINIDUMP_THREAD_LIST</a>



<a href="https://msdn.microsoft.com/26a42ae7-f84d-451d-92e9-dbaffb15ca74">MINIDUMP_UNLOADED_MODULE_LIST</a>



<a href="https://msdn.microsoft.com/43eae98c-fba3-43a4-97e6-8b81874e856e">MINIDUMP_USER_STREAM</a>
 

 

