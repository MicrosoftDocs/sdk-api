---
UID: NE:minidumpapiset._MINIDUMP_CALLBACK_TYPE
title: MINIDUMP_CALLBACK_TYPE (minidumpapiset.h)
description: Identifies the type of information returned by the MiniDumpCallback function.
helpviewer_keywords: ["CancelCallback","IncludeModuleCallback","IncludeThreadCallback","IncludeVmRegionCallback","IoFinishCallback","IoStartCallback","IoWriteAllCallback","IsProcessSnapshotCallback","KernelMinidumpStatusCallback","MINIDUMP_CALLBACK_TYPE","MINIDUMP_CALLBACK_TYPE enumeration","MemoryCallback","ModuleCallback","ReadMemoryFailureCallback","RemoveMemoryCallback","SecondaryFlagsCallback","ThreadCallback","ThreadExCallback","VmPostReadCallback","VmPreReadCallback","VmQueryCallback","VmStartCallback","WriteKernelMinidumpCallback","_win32_minidump_callback_type","base.minidump_callback_type","minidumpapiset/CancelCallback","minidumpapiset/IncludeModuleCallback","minidumpapiset/IncludeThreadCallback","minidumpapiset/IncludeVmRegionCallback","minidumpapiset/IoFinishCallback","minidumpapiset/IoStartCallback","minidumpapiset/IoWriteAllCallback","minidumpapiset/IsProcessSnapshotCallback","minidumpapiset/KernelMinidumpStatusCallback","minidumpapiset/MINIDUMP_CALLBACK_TYPE","minidumpapiset/MemoryCallback","minidumpapiset/ModuleCallback","minidumpapiset/ReadMemoryFailureCallback","minidumpapiset/RemoveMemoryCallback","minidumpapiset/SecondaryFlagsCallback","minidumpapiset/ThreadCallback","minidumpapiset/ThreadExCallback","minidumpapiset/VmPostReadCallback","minidumpapiset/VmPreReadCallback","minidumpapiset/VmQueryCallback","minidumpapiset/VmStartCallback","minidumpapiset/WriteKernelMinidumpCallback"]
old-location: base\minidump_callback_type.htm
tech.root: Debug
ms.assetid: c970564d-e1f0-4317-bf66-752b98767451
ms.date: 12/05/2018
ms.keywords: CancelCallback, IncludeModuleCallback, IncludeThreadCallback, IncludeVmRegionCallback, IoFinishCallback, IoStartCallback, IoWriteAllCallback, IsProcessSnapshotCallback, KernelMinidumpStatusCallback, MINIDUMP_CALLBACK_TYPE, MINIDUMP_CALLBACK_TYPE enumeration, MemoryCallback, ModuleCallback, ReadMemoryFailureCallback, RemoveMemoryCallback, SecondaryFlagsCallback, ThreadCallback, ThreadExCallback, VmPostReadCallback, VmPreReadCallback, VmQueryCallback, VmStartCallback, WriteKernelMinidumpCallback, _win32_minidump_callback_type, base.minidump_callback_type, minidumpapiset/CancelCallback, minidumpapiset/IncludeModuleCallback, minidumpapiset/IncludeThreadCallback, minidumpapiset/IncludeVmRegionCallback, minidumpapiset/IoFinishCallback, minidumpapiset/IoStartCallback, minidumpapiset/IoWriteAllCallback, minidumpapiset/IsProcessSnapshotCallback, minidumpapiset/KernelMinidumpStatusCallback, minidumpapiset/MINIDUMP_CALLBACK_TYPE, minidumpapiset/MemoryCallback, minidumpapiset/ModuleCallback, minidumpapiset/ReadMemoryFailureCallback, minidumpapiset/RemoveMemoryCallback, minidumpapiset/SecondaryFlagsCallback, minidumpapiset/ThreadCallback, minidumpapiset/ThreadExCallback, minidumpapiset/VmPostReadCallback, minidumpapiset/VmPreReadCallback, minidumpapiset/VmQueryCallback, minidumpapiset/VmStartCallback, minidumpapiset/WriteKernelMinidumpCallback
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
req.typenames: MINIDUMP_CALLBACK_TYPE
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_CALLBACK_TYPE
 - minidumpapiset/_MINIDUMP_CALLBACK_TYPE
 - MINIDUMP_CALLBACK_TYPE
 - minidumpapiset/MINIDUMP_CALLBACK_TYPE
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
 - MINIDUMP_CALLBACK_TYPE
---

# MINIDUMP_CALLBACK_TYPE enumeration


## -description

Identifies the type of information returned by the 
    <a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a> function. Not all memory 
    failures will cause a callback; for example if the failure is within a stack then the failure is considered to be 
    unrecoverable and the minidump will fail.

## -enum-fields

### -field ModuleCallback

The callback function returns module information.

### -field ThreadCallback

The callback function returns thread information.

### -field ThreadExCallback

The callback function returns extended thread information.

### -field IncludeThreadCallback

The callback function indicates which threads are to be included. It is called as the minidump library is 
      enumerating the threads in a process, rather than after the information gathered, as it is with 
      <b>ThreadCallback</b> or <b>ThreadExCallback</b>. It is called for 
      each thread. If the callback function returns <b>FALSE</b>, the current thread is excluded. 
      This allows the caller to obtain information for a subset of the threads in a process, without suspending 
      threads that are not of interest. Alternately, you can modify the <b>ThreadWriteFlags</b> 
      member of the <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> 
      structure and return <b>TRUE</b> to avoid gathering unnecessary information for the 
      thread.

### -field IncludeModuleCallback

The callback function indicates which modules are to be included. The callback function is called as the 
      minidump library is enumerating the modules in a process, rather than after the information is gathered, as it 
      is with <b>ModuleCallback</b>. It is called for each module. If the callback function 
      returns <b>FALSE</b>, the current module is excluded. Alternatively, you can modify the 
      <b>ModuleWriteFlags</b> member of the 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> structure and 
      return <b>TRUE</b> to avoid gathering unnecessary information for the module.

### -field MemoryCallback

The callback function returns a region of memory to be included in the dump. The callback is called only 
      for dumps generated without the MiniDumpWithFullMemory flag. If the callback function returns 
      <b>FALSE</b> or a region of size 0, the callback will not be called again.
      

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field CancelCallback

The callback function returns cancellation information.
      

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field WriteKernelMinidumpCallback

The user-mode minidump has been successfully completed. To initiate a kernel-mode minidump, the callback 
      should return <b>TRUE</b> and set the <b>Handle</b> member of the 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> structure.
      

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field KernelMinidumpStatusCallback

The callback function returns status information for the kernel minidump.
      

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field RemoveMemoryCallback

The callback function returns a region of memory to be excluded from the dump. The callback is called only 
      for dumps generated without the <b>MiniDumpWithFullMemory</b> flag. If the callback 
      function returns <b>FALSE</b> or a region of size 0, the callback will not be called again.
      

<b>DbgHelp 6.3 and earlier:  </b>This value is not supported.

### -field IncludeVmRegionCallback

The callback function returns information about the virtual memory region. It is called twice for each 
      region during the full-memory writing pass. The <b>VmRegion</b> member of the 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> structure 
      contains the current memory region. You can modify the base address and size of the region, as long as the new 
      region remains a subset of the original region; changes to other members are ignored. If the callback returns 
      <b>TRUE</b> and sets the <b>Continue</b> member of 
      <b>MINIDUMP_CALLBACK_OUTPUT</b> to 
      <b>TRUE</b>, the minidump library will use the region specified by 
      <b>VmRegion</b> as the region to be written. If the callback returns 
      <b>FALSE</b> or if <b>Continue</b> is <b>FALSE</b>, 
      the callback will not be called for additional memory regions.
      

<b>DbgHelp 6.4 and earlier:  </b>This value is not supported.

### -field IoStartCallback

The callback function indicates that the caller will be providing an alternate I/O routine. If the callback 
      returns <b>TRUE</b> and sets the <b>Status</b> member of 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> to 
      <b>S_FALSE</b>, the minidump library will send all I/O through callbacks. The caller will 
      receive an <b>IoWriteAllCallback</b> callback for each piece of data.
      

<b>DbgHelp 6.4 and earlier:  </b>This value is not supported.

### -field IoWriteAllCallback

The callback must write all requested bytes or fail. The <b>Io</b> member of the 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_input">MINIDUMP_CALLBACK_INPUT</a> structure contains 
      the request. If the write operation fails, the callback should return <b>FALSE</b>.  If the 
      write operation succeeds, the callback should return <b>TRUE</b> and set the 
      <b>Status</b> member of 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> to 
      <b>S_OK</b>. The caller will receive an <b>IoFinishCallback</b> callback 
      when the I/O has completed.
      

<b>DbgHelp 6.4 and earlier:  </b>This value is not supported.

### -field IoFinishCallback

The callback returns I/O completion information. If the callback returns <b>FALSE</b> or 
      does not set the <b>Status</b> member of 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> to 
      <b>S_OK</b>, the minidump library assumes the minidump write operation has failed.
      

<b>DbgHelp 6.4 and earlier:  </b>This value is not supported.

### -field ReadMemoryFailureCallback

There has been a failure to read memory. If the callback returns <b>TRUE</b> and sets 
      the <b>Status</b> member of 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> to 
      <b>S_OK</b>, the memory failure is ignored and the block is omitted from the minidump. Otherwise, this 
      failure results in a failure to write to the minidump.
      

<b>DbgHelp 6.4 and earlier:  </b>This value is not supported.

### -field SecondaryFlagsCallback

The callback returns secondary information.
      

<b>DbgHelp 6.5 and earlier:  </b>This value is not supported.

### -field IsProcessSnapshotCallback

The callback function indicates whether the target is a process or a snapshot.

<b>DbgHelp 6.2 and earlier:  </b>This value is not supported.

### -field VmStartCallback

The callback function indicates whether the callee supports and accepts virtual memory callbacks, such as <b>VmQueryCallback</b>, <b>VmPreReadCallback</b>, and <b>VmPostReadCallback</b>.
 
A return value of S_FALSE means that virtual memory callbacks are supported. A value of S_OK means that virtual memory callbacks are not supported.

<b>DbgHelp 6.2 and earlier:  </b>This value is not supported.

### -field VmQueryCallback

The callback function  is invoked for snapshot targets to collect virtual address memory information from the target.
The callback is only called if <b>VmStartCallback</b> returned a value of S_FALSE.


<b>DbgHelp 6.2 and earlier:  </b>This value is not supported.

### -field VmPreReadCallback

The callback function is sent for every ReadVirtual operation. These reads are not limited to the memory blocks that are added to the dump. The engine also accesses the Process Environment Block (PEB), the Thread Environment Block (TEB), the loader data, the unloaded module traces, and other blocks. Even if those blocks do not end up in the dump, they are read from the target, and virtual memory callbacks are initiated for each. The callback is only called if <b>VmStartCallback</b> returned S_FALSE.

<b>DbgHelp 6.2 and earlier:  </b>This value is not supported.

### -field VmPostReadCallback

The callback function allows the callee to alter the buffer contents with data from other sources, such as a cache, or perform obfuscation. The buffer at this point is fully or partially filled by <b>VmPreReadCallback</b> and by <b>ReadProcessMemory</b>. The callback is only called if <b>VmStartCallback</b> returned S_FALSE.

<b>DbgHelp 6.2 and earlier:  </b>This value is not supported.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_input">MINIDUMP_CALLBACK_INPUT</a>



<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>