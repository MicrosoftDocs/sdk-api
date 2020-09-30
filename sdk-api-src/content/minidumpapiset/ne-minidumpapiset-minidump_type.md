---
UID: NE:minidumpapiset._MINIDUMP_TYPE
title: MINIDUMP_TYPE (minidumpapiset.h)
description: Identifies the type of information that will be written to the minidump file by the MiniDumpWriteDump function.
helpviewer_keywords: ["MINIDUMP_TYPE","MINIDUMP_TYPE enumeration","MiniDumpFilterMemory","MiniDumpFilterModulePaths","MiniDumpFilterTriage","MiniDumpIgnoreInaccessibleMemory","MiniDumpNormal","MiniDumpScanMemory","MiniDumpValidTypeFlags","MiniDumpWithCodeSegs","MiniDumpWithDataSegs","MiniDumpWithFullAuxiliaryState","MiniDumpWithFullMemory","MiniDumpWithFullMemoryInfo","MiniDumpWithHandleData","MiniDumpWithIndirectlyReferencedMemory","MiniDumpWithModuleHeaders","MiniDumpWithPrivateReadWriteMemory","MiniDumpWithPrivateWriteCopyMemory","MiniDumpWithProcessThreadData","MiniDumpWithThreadInfo","MiniDumpWithTokenInformation","MiniDumpWithUnloadedModules","MiniDumpWithoutAuxiliaryState","MiniDumpWithoutOptionalData","_win32_minidump_type","base.minidump_type","minidumpapiset/MINIDUMP_TYPE","minidumpapiset/MiniDumpFilterMemory","minidumpapiset/MiniDumpFilterModulePaths","minidumpapiset/MiniDumpFilterTriage","minidumpapiset/MiniDumpIgnoreInaccessibleMemory","minidumpapiset/MiniDumpNormal","minidumpapiset/MiniDumpScanMemory","minidumpapiset/MiniDumpValidTypeFlags","minidumpapiset/MiniDumpWithCodeSegs","minidumpapiset/MiniDumpWithDataSegs","minidumpapiset/MiniDumpWithFullAuxiliaryState","minidumpapiset/MiniDumpWithFullMemory","minidumpapiset/MiniDumpWithFullMemoryInfo","minidumpapiset/MiniDumpWithHandleData","minidumpapiset/MiniDumpWithIndirectlyReferencedMemory","minidumpapiset/MiniDumpWithModuleHeaders","minidumpapiset/MiniDumpWithPrivateReadWriteMemory","minidumpapiset/MiniDumpWithPrivateWriteCopyMemory","minidumpapiset/MiniDumpWithProcessThreadData","minidumpapiset/MiniDumpWithThreadInfo","minidumpapiset/MiniDumpWithTokenInformation","minidumpapiset/MiniDumpWithUnloadedModules","minidumpapiset/MiniDumpWithoutAuxiliaryState","minidumpapiset/MiniDumpWithoutOptionalData"]
old-location: base\minidump_type.htm
tech.root: Debug
ms.assetid: 89ae3a75-5f02-4c5e-9d72-95fb8ef94985
ms.date: 12/05/2018
ms.keywords: MINIDUMP_TYPE, MINIDUMP_TYPE enumeration, MiniDumpFilterMemory, MiniDumpFilterModulePaths, MiniDumpFilterTriage, MiniDumpIgnoreInaccessibleMemory, MiniDumpNormal, MiniDumpScanMemory, MiniDumpValidTypeFlags, MiniDumpWithCodeSegs, MiniDumpWithDataSegs, MiniDumpWithFullAuxiliaryState, MiniDumpWithFullMemory, MiniDumpWithFullMemoryInfo, MiniDumpWithHandleData, MiniDumpWithIndirectlyReferencedMemory, MiniDumpWithModuleHeaders, MiniDumpWithPrivateReadWriteMemory, MiniDumpWithPrivateWriteCopyMemory, MiniDumpWithProcessThreadData, MiniDumpWithThreadInfo, MiniDumpWithTokenInformation, MiniDumpWithUnloadedModules, MiniDumpWithoutAuxiliaryState, MiniDumpWithoutOptionalData, _win32_minidump_type, base.minidump_type, minidumpapiset/MINIDUMP_TYPE, minidumpapiset/MiniDumpFilterMemory, minidumpapiset/MiniDumpFilterModulePaths, minidumpapiset/MiniDumpFilterTriage, minidumpapiset/MiniDumpIgnoreInaccessibleMemory, minidumpapiset/MiniDumpNormal, minidumpapiset/MiniDumpScanMemory, minidumpapiset/MiniDumpValidTypeFlags, minidumpapiset/MiniDumpWithCodeSegs, minidumpapiset/MiniDumpWithDataSegs, minidumpapiset/MiniDumpWithFullAuxiliaryState, minidumpapiset/MiniDumpWithFullMemory, minidumpapiset/MiniDumpWithFullMemoryInfo, minidumpapiset/MiniDumpWithHandleData, minidumpapiset/MiniDumpWithIndirectlyReferencedMemory, minidumpapiset/MiniDumpWithModuleHeaders, minidumpapiset/MiniDumpWithPrivateReadWriteMemory, minidumpapiset/MiniDumpWithPrivateWriteCopyMemory, minidumpapiset/MiniDumpWithProcessThreadData, minidumpapiset/MiniDumpWithThreadInfo, minidumpapiset/MiniDumpWithTokenInformation, minidumpapiset/MiniDumpWithUnloadedModules, minidumpapiset/MiniDumpWithoutAuxiliaryState, minidumpapiset/MiniDumpWithoutOptionalData
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
req.typenames: MINIDUMP_TYPE
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_TYPE
 - minidumpapiset/_MINIDUMP_TYPE
 - MINIDUMP_TYPE
 - minidumpapiset/MINIDUMP_TYPE
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
 - MINIDUMP_TYPE
---

# MINIDUMP_TYPE enumeration


## -description

Identifies the type of information that will be written to the minidump file by the 
    <a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function.<div class="alert"><b>Important</b>  <p class="note">The minidump code has evolved greatly over the years since its inception.  Many of the 
     constants listed on this page were added later and are not available in all versions of DbgHelp.dll. 
     Those that did not exist in the original code are labeled accordingly along with the version of DbgHelp.dll that 
     they first were implemented in. The listed version numbers corresponds to the 
     Debugging Tools For Windows releases and do not 
     apply to copies of DbgHelp.dll that are integrated into Windows. See 
     <a href="/windows/desktop/Debug/dbghelp-versions">DbgHelp Versions</a> for more details.

</div>
<div> </div>

## -enum-fields

### -field MiniDumpNormal

Include just the information necessary to capture stack traces for all existing threads in a process.

### -field MiniDumpWithDataSegs

Include the data sections from all loaded modules. This results in the inclusion of global variables, which 
      can make the minidump file significantly larger. For per-module control, use the 
      <b>ModuleWriteDataSeg</b> enumeration value from 
      <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-module_write_flags">MODULE_WRITE_FLAGS</a>.

### -field MiniDumpWithFullMemory

Include all accessible memory in the process. The raw memory data is included at the end, so that the 
      initial structures can be mapped directly without the raw memory information. This option can result in a very 
      large file.

### -field MiniDumpWithHandleData

Include high-level information about the operating system handles that are active when the minidump is 
      made.

### -field MiniDumpFilterMemory

Stack and backing store memory written to the minidump file should be filtered to remove all but the 
      pointer values necessary to reconstruct a stack trace.

### -field MiniDumpScanMemory

Stack and backing store memory should be scanned for pointer references to modules in the module list. If a 
      module is referenced by stack or backing store memory, the <b>ModuleWriteFlags</b> member of 
      the <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a> structure is 
      set to <b>ModuleReferencedByMemory</b>.

### -field MiniDumpWithUnloadedModules

Include information from the list of modules that were recently unloaded, if this information is maintained 
      by the operating system.
      

<b>Windows Server 2003 and Windows XP:  </b>The operating system does not maintain information for unloaded modules until 
        Windows Server 2003 with SP1 and Windows XP with SP2.

<b>DbgHelp 5.1:  </b>This value is not supported.

### -field MiniDumpWithIndirectlyReferencedMemory

Include pages with data referenced by locals or other stack memory. This option can increase the size of 
      the minidump file significantly.
      

<b>DbgHelp 5.1:  </b>This value is not supported.

### -field MiniDumpFilterModulePaths

Filter module paths for information such as user names or important directories. This option may prevent 
      the system from locating the image file and should be used only in special situations.
      

<b>DbgHelp 5.1:  </b>This value is not supported.

### -field MiniDumpWithProcessThreadData

Include complete per-process and per-thread information from the operating system.
      

<b>DbgHelp 5.1:  </b>This value is not supported.

### -field MiniDumpWithPrivateReadWriteMemory

Scan the virtual address space for <b>PAGE_READWRITE</b> memory to be included.
      

<b>DbgHelp 5.1:  </b>This value is not supported.

### -field MiniDumpWithoutOptionalData

Reduce the data that is dumped by eliminating memory regions that are not essential to meet criteria  
      specified for the dump. This can avoid dumping  memory that may contain data that is private to the user. 
      However, it is not a guarantee that no private information will be present.
      

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field MiniDumpWithFullMemoryInfo

Include memory region information. For more information, see 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_memory_info_list">MINIDUMP_MEMORY_INFO_LIST</a>.
      

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field MiniDumpWithThreadInfo

Include thread state information. For more information, see 
      <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_info_list">MINIDUMP_THREAD_INFO_LIST</a>.
      

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field MiniDumpWithCodeSegs

Include all code and code-related sections from loaded modules to capture executable content. For 
      per-module control, use the <b>ModuleWriteCodeSegs</b> enumeration value from 
      <a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-module_write_flags">MODULE_WRITE_FLAGS</a>.
      

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

### -field MiniDumpWithoutAuxiliaryState

Turns off secondary auxiliary-supported memory gathering.

### -field MiniDumpWithFullAuxiliaryState

Requests that auxiliary data providers include their state in the dump image; the state data that is 
      included is provider dependent. This option can result in a large dump image.

### -field MiniDumpWithPrivateWriteCopyMemory

Scans the virtual address space for <b>PAGE_WRITECOPY</b> memory to be included.
      

<b>Prior to DbgHelp 6.1:  </b>This value is not supported.

### -field MiniDumpIgnoreInaccessibleMemory

If you specify <b>MiniDumpWithFullMemory</b>, the 
       <a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function will fail if the 
       function cannot read the memory regions; however, if you include 
       <b>MiniDumpIgnoreInaccessibleMemory</b>, the 
       <b>MiniDumpWriteDump</b> function will ignore the memory 
       read failures and continue to generate the dump. Note that the inaccessible memory regions are not included in 
       the dump.

<b>Prior to DbgHelp 6.1:  </b>This value is not supported.

### -field MiniDumpWithTokenInformation

Adds security token related data. This will make the "!token" extension work when 
      processing a user-mode dump.
      

<b>Prior to DbgHelp 6.1:  </b>This value is not supported.

### -field MiniDumpWithModuleHeaders

Adds module header related data.
      

<b>Prior to DbgHelp 6.1:  </b>This value is not supported.

### -field MiniDumpFilterTriage

Adds filter triage related data.
      

<b>Prior to DbgHelp 6.1:  </b>This value is not supported.

### -field MiniDumpWithAvxXStateContext

### -field MiniDumpWithIptTrace

### -field MiniDumpValidTypeFlags

Indicates which flags are valid.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>