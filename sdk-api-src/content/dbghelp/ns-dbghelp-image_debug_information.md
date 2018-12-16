---
UID: NS:dbghelp._IMAGE_DEBUG_INFORMATION
title: IMAGE_DEBUG_INFORMATION
author: windows-sdk-content
description: Contains debugging information.
old-location: base\image_debug_information_str.htm
tech.root: debug
ms.assetid: f8db7695-4967-45c0-a6bf-019e825bd9ab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PIMAGE_DEBUG_INFORMATION, IMAGE_DEBUG_INFORMATION, IMAGE_DEBUG_INFORMATION structure, IMAGE_FILE_32BIT_MACHINE, IMAGE_FILE_AGGRESIVE_WS_TRIM, IMAGE_FILE_BYTES_REVERSED_HI, IMAGE_FILE_BYTES_REVERSED_LO, IMAGE_FILE_DEBUG_STRIPPED, IMAGE_FILE_DLL, IMAGE_FILE_EXECUTABLE_IMAGE, IMAGE_FILE_LARGE_ADDRESS_AWARE, IMAGE_FILE_LINE_NUMS_STRIPPED, IMAGE_FILE_LOCAL_SYMS_STRIPPED, IMAGE_FILE_MACHINE_AMD64, IMAGE_FILE_MACHINE_I386, IMAGE_FILE_MACHINE_IA64, IMAGE_FILE_NET_RUN_FROM_SWAP, IMAGE_FILE_RELOCS_STRIPPED, IMAGE_FILE_REMOVABLE_RUN_FROM_SWAP, IMAGE_FILE_SYSTEM, IMAGE_FILE_UP_SYSTEM_ONLY, LIST_ENTRY, PIMAGE_DEBUG_INFORMATION, PIMAGE_DEBUG_INFORMATION structure pointer, _IMAGE_DEBUG_INFORMATION, _win32_image_debug_information_str, base.image_debug_information_str, dbghelp/IMAGE_DEBUG_INFORMATION, dbghelp/PIMAGE_DEBUG_INFORMATION"
ms.topic: struct
req.header: dbghelp.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - IMAGE_DEBUG_INFORMATION
product: Windows
targetos: Windows
req.typenames: IMAGE_DEBUG_INFORMATION, *PIMAGE_DEBUG_INFORMATION
req.redist: DbgHelp.dll 5.1 or later
---

# IMAGE_DEBUG_INFORMATION structure


## -description


Contains debugging information.
<div class="alert"><b>Note</b>  This structure is used by the 
    <a href="https://msdn.microsoft.com/749a2a99-f6c4-4af3-aa0b-8a7bb5c690da">MapDebugInformation</a> and 
    <a href="https://msdn.microsoft.com/86d82f23-7803-475f-8b23-c3964d33cb00">UnmapDebugInformation</a> functions, which are 
    provided only for backward compatibility.</div><div> </div>

## -struct-fields




### -field List

A linked list of <b>LIST_ENTRY</b> structures.


### -field ReservedSize

The size of the memory allocated for the 
      <b>IMAGE_DEBUG_INFORMATION</b> structure and all 
      debugging information, in bytes.


### -field ReservedMappedBase

The base address of the image.


### -field ReservedMachine

The computer type. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_MACHINE_I386"></a><a id="image_file_machine_i386"></a><dl>
<dt><b>IMAGE_FILE_MACHINE_I386</b></dt>
<dt>0x014c</dt>
</dl>
</td>
<td width="60%">
Intel (32-bit)

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_MACHINE_IA64"></a><a id="image_file_machine_ia64"></a><dl>
<dt><b>IMAGE_FILE_MACHINE_IA64</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Intel Itanium

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_MACHINE_AMD64"></a><a id="image_file_machine_amd64"></a><dl>
<dt><b>IMAGE_FILE_MACHINE_AMD64</b></dt>
<dt>0x8664</dt>
</dl>
</td>
<td width="60%">
x64 (AMD64 or EM64T)

</td>
</tr>
</table>
 


### -field ReservedCharacteristics

The characteristics of the image. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_RELOCS_STRIPPED"></a><a id="image_file_relocs_stripped"></a><dl>
<dt><b>IMAGE_FILE_RELOCS_STRIPPED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Relocation information is stripped from the file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_EXECUTABLE_IMAGE"></a><a id="image_file_executable_image"></a><dl>
<dt><b>IMAGE_FILE_EXECUTABLE_IMAGE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The file is executable (there are no unresolved external references).

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_LINE_NUMS_STRIPPED"></a><a id="image_file_line_nums_stripped"></a><dl>
<dt><b>IMAGE_FILE_LINE_NUMS_STRIPPED</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Line numbers are stripped from the file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_LOCAL_SYMS_STRIPPED"></a><a id="image_file_local_syms_stripped"></a><dl>
<dt><b>IMAGE_FILE_LOCAL_SYMS_STRIPPED</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Local symbols are stripped from file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_AGGRESIVE_WS_TRIM"></a><a id="image_file_aggresive_ws_trim"></a><dl>
<dt><b>IMAGE_FILE_AGGRESIVE_WS_TRIM</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Aggressively trim the working set.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_LARGE_ADDRESS_AWARE"></a><a id="image_file_large_address_aware"></a><dl>
<dt><b>IMAGE_FILE_LARGE_ADDRESS_AWARE</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The application can handle addresses larger than 2 GB.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_BYTES_REVERSED_LO"></a><a id="image_file_bytes_reversed_lo"></a><dl>
<dt><b>IMAGE_FILE_BYTES_REVERSED_LO</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Bytes of the word are reversed.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_32BIT_MACHINE"></a><a id="image_file_32bit_machine"></a><dl>
<dt><b>IMAGE_FILE_32BIT_MACHINE</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Computer supports 32-bit words.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_DEBUG_STRIPPED"></a><a id="image_file_debug_stripped"></a><dl>
<dt><b>IMAGE_FILE_DEBUG_STRIPPED</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Debugging information is stored separately in a .dbg file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_REMOVABLE_RUN_FROM_SWAP"></a><a id="image_file_removable_run_from_swap"></a><dl>
<dt><b>IMAGE_FILE_REMOVABLE_RUN_FROM_SWAP</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
If the image is on removable media, copy and run from the swap file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_NET_RUN_FROM_SWAP"></a><a id="image_file_net_run_from_swap"></a><dl>
<dt><b>IMAGE_FILE_NET_RUN_FROM_SWAP</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
If the image is on the network, copy and run from the swap file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_SYSTEM"></a><a id="image_file_system"></a><dl>
<dt><b>IMAGE_FILE_SYSTEM</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
System file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_DLL"></a><a id="image_file_dll"></a><dl>
<dt><b>IMAGE_FILE_DLL</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
DLL file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_UP_SYSTEM_ONLY"></a><a id="image_file_up_system_only"></a><dl>
<dt><b>IMAGE_FILE_UP_SYSTEM_ONLY</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
File should be run only on a uniprocessor computer.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_BYTES_REVERSED_HI"></a><a id="image_file_bytes_reversed_hi"></a><dl>
<dt><b>IMAGE_FILE_BYTES_REVERSED_HI</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Bytes of the word are reversed.

</td>
</tr>
</table>
 


### -field ReservedCheckSum

The checksum of the image.


### -field ImageBase

The requested base address of the image.


### -field SizeOfImage

The size of the image, in bytes.


### -field ReservedNumberOfSections

The number of COFF section headers.


### -field ReservedSections

A pointer to the first COFF section header. For more information, see 
      <a href="https://msdn.microsoft.com/81ddf56d-66cc-4a0c-9cff-a84376a3223d">IMAGE_SECTION_HEADER</a>.


### -field ReservedExportedNamesSize

The size of the <b>ExportedNames</b> member, in bytes.


### -field ReservedExportedNames

A pointer to a series of null-terminated strings that name all the functions exported from the image.


### -field ReservedNumberOfFunctionTableEntries

The number of entries contained in the <b>FunctionTableEntries</b> member.


### -field ReservedFunctionTableEntries

A pointer to the first function table entry. For more information, see 
      <a href="https://msdn.microsoft.com/ced956ec-7a12-4548-8e38-a1c1057c05e8">IMAGE_FUNCTION_ENTRY</a>.


### -field ReservedLowestFunctionStartingAddress

The lowest function table starting address.


### -field ReservedHighestFunctionEndingAddress

The highest function table ending address.


### -field ReservedNumberOfFpoTableEntries

The number of entries contained in the <b>FpoTableEntries</b> member.


### -field ReservedFpoTableEntries

A pointer to the first FPO entry. For more information, see 
      <a href="https://msdn.microsoft.com/916dc7d5-ed88-4573-b696-fd00bbf4e086">FPO_DATA</a>.


### -field SizeOfCoffSymbols

The size of the COFF symbol table, in bytes.


### -field CoffSymbols

A pointer to the COFF symbol table.


### -field ReservedSizeOfCodeViewSymbols

The size of the CodeView symbol table, in bytes.


### -field ReservedCodeViewSymbols

A pointer to the beginning of the CodeView symbol table.


### -field ImageFilePath

The relative path to the image file name.


### -field ImageFileName

The image file name.


### -field ReservedDebugFilePath

The full path to the symbol file.


### -field ReservedTimeDateStamp

The timestamp of the image. This represents the date and time the image was created by the linker.


### -field ReservedRomImage

This value is <b>TRUE</b> if the image is a ROM image.


### -field ReservedDebugDirectory

A pointer to the first debug directory. For more information, see 
      <a href="https://msdn.microsoft.com/f89a3c9b-4d73-4ff5-8f45-2e58500d5084">IMAGE_DEBUG_DIRECTORY</a>.


### -field ReservedNumberOfDebugDirectories

The number of entries contained in the <b>DebugDirectory</b> member.


### -field ReservedOriginalFunctionTableBaseAddress

The original function table base address.


### -field Reserved

This member is reserved for use by the operating system.


## -remarks



The <b>LIST_ENTRY</b> structure is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef struct _LIST_ENTRY {
   struct _LIST_ENTRY *Flink;
   struct _LIST_ENTRY *Blink;
} LIST_ENTRY, *PLIST_ENTRY, *RESTRICTED_POINTER PRLIST_ENTRY;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/916dc7d5-ed88-4573-b696-fd00bbf4e086">FPO_DATA</a>



<a href="https://msdn.microsoft.com/f3a0ba0e-ef6b-4355-8dc4-5099dd54ab7e">IMAGE_COFF_SYMBOLS_HEADER</a>



<a href="https://msdn.microsoft.com/f89a3c9b-4d73-4ff5-8f45-2e58500d5084">IMAGE_DEBUG_DIRECTORY</a>



<a href="https://msdn.microsoft.com/ced956ec-7a12-4548-8e38-a1c1057c05e8">IMAGE_FUNCTION_ENTRY</a>



<a href="https://msdn.microsoft.com/81ddf56d-66cc-4a0c-9cff-a84376a3223d">IMAGE_SECTION_HEADER</a>



<a href="https://msdn.microsoft.com/749a2a99-f6c4-4af3-aa0b-8a7bb5c690da">MapDebugInformation</a>



<a href="https://msdn.microsoft.com/86d82f23-7803-475f-8b23-c3964d33cb00">UnmapDebugInformation</a>
 

 

