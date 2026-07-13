---
UID: NS:winnt._IMAGE_FILE_HEADER
title: IMAGE_FILE_HEADER (winnt.h)
description: Represents the COFF header format.
helpviewer_keywords: ["*PIMAGE_FILE_HEADER","IMAGE_FILE_32BIT_MACHINE","IMAGE_FILE_AGGRESIVE_WS_TRIM","IMAGE_FILE_BYTES_REVERSED_HI","IMAGE_FILE_BYTES_REVERSED_LO","IMAGE_FILE_DEBUG_STRIPPED","IMAGE_FILE_DLL","IMAGE_FILE_EXECUTABLE_IMAGE","IMAGE_FILE_HEADER","IMAGE_FILE_HEADER structure","IMAGE_FILE_LARGE_ADDRESS_AWARE","IMAGE_FILE_LINE_NUMS_STRIPPED","IMAGE_FILE_LOCAL_SYMS_STRIPPED","IMAGE_FILE_MACHINE_AMD64","IMAGE_FILE_MACHINE_I386","IMAGE_FILE_MACHINE_IA64","IMAGE_FILE_NET_RUN_FROM_SWAP","IMAGE_FILE_RELOCS_STRIPPED","IMAGE_FILE_REMOVABLE_RUN_FROM_SWAP","IMAGE_FILE_SYSTEM","IMAGE_FILE_UP_SYSTEM_ONLY","PIMAGE_FILE_HEADER","PIMAGE_FILE_HEADER structure pointer","_IMAGE_FILE_HEADER","_win32_image_file_header_str","base.image_file_header_str","winnt/IMAGE_FILE_HEADER","winnt/PIMAGE_FILE_HEADER"]
old-location: base\image_file_header_str.htm
tech.root: Debug
ms.assetid: 1f1fe842-0849-46d0-8dba-831cf5aa02ef
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_FILE_HEADER, IMAGE_FILE_32BIT_MACHINE, IMAGE_FILE_AGGRESIVE_WS_TRIM, IMAGE_FILE_BYTES_REVERSED_HI, IMAGE_FILE_BYTES_REVERSED_LO, IMAGE_FILE_DEBUG_STRIPPED, IMAGE_FILE_DLL, IMAGE_FILE_EXECUTABLE_IMAGE, IMAGE_FILE_HEADER, IMAGE_FILE_HEADER structure, IMAGE_FILE_LARGE_ADDRESS_AWARE, IMAGE_FILE_LINE_NUMS_STRIPPED, IMAGE_FILE_LOCAL_SYMS_STRIPPED, IMAGE_FILE_MACHINE_AMD64, IMAGE_FILE_MACHINE_I386, IMAGE_FILE_MACHINE_IA64, IMAGE_FILE_NET_RUN_FROM_SWAP, IMAGE_FILE_RELOCS_STRIPPED, IMAGE_FILE_REMOVABLE_RUN_FROM_SWAP, IMAGE_FILE_SYSTEM, IMAGE_FILE_UP_SYSTEM_ONLY, PIMAGE_FILE_HEADER, PIMAGE_FILE_HEADER structure pointer, _IMAGE_FILE_HEADER, _win32_image_file_header_str, base.image_file_header_str, winnt/IMAGE_FILE_HEADER, winnt/PIMAGE_FILE_HEADER'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: IMAGE_FILE_HEADER, *PIMAGE_FILE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_FILE_HEADER
 - winnt/_IMAGE_FILE_HEADER
 - PIMAGE_FILE_HEADER
 - winnt/PIMAGE_FILE_HEADER
 - IMAGE_FILE_HEADER
 - winnt/IMAGE_FILE_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - IMAGE_FILE_HEADER
---

# IMAGE_FILE_HEADER structure


## -description

Represents the COFF header format.

## -struct-fields

### -field Machine

The architecture type of the computer. An image file can only be run on the specified computer or a system 
      that emulates the specified computer. This member can be one of the following values.

For a complete list of valid Machine types and supported architectures, see the [PE Format](/windows/win32/debug/pe-format#machine-types) documentation.

### -field NumberOfSections

The number of sections. This indicates the size of the section table, which immediately follows the 
      headers. Note that the Windows loader limits the number of sections to 96.

### -field TimeDateStamp

The low 32 bits of the time stamp of the image. This represents the date and time the image was created by 
      the linker. The value is represented in the number of seconds elapsed since midnight (00:00:00), January 1, 
      1970, Universal Coordinated Time, according to the system clock.

### -field PointerToSymbolTable

The offset of the symbol table, in bytes, or zero if no COFF symbol table exists.

### -field NumberOfSymbols

The number of symbols in the symbol table.

### -field SizeOfOptionalHeader

The size of the optional header, in bytes. This value should be 0 for object files.

### -field Characteristics

The characteristics of the image. This member can be one or more of the following values.

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
Relocation information was stripped from the file. The file must be loaded at its preferred base address. 
        If the base address is not available, the loader reports an error.

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
COFF line numbers were stripped from the file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_LOCAL_SYMS_STRIPPED"></a><a id="image_file_local_syms_stripped"></a><dl>
<dt><b>IMAGE_FILE_LOCAL_SYMS_STRIPPED</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
COFF symbol table entries were stripped from file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_AGGRESIVE_WS_TRIM"></a><a id="image_file_aggresive_ws_trim"></a><dl>
<dt><b>IMAGE_FILE_AGGRESIVE_WS_TRIM</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Aggressively trim the working set. This value is obsolete.

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
The bytes of the word are reversed. This flag is obsolete.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_32BIT_MACHINE"></a><a id="image_file_32bit_machine"></a><dl>
<dt><b>IMAGE_FILE_32BIT_MACHINE</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
The computer supports 32-bit words.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_DEBUG_STRIPPED"></a><a id="image_file_debug_stripped"></a><dl>
<dt><b>IMAGE_FILE_DEBUG_STRIPPED</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Debugging information was removed and stored separately in another file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_REMOVABLE_RUN_FROM_SWAP"></a><a id="image_file_removable_run_from_swap"></a><dl>
<dt><b>IMAGE_FILE_REMOVABLE_RUN_FROM_SWAP</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
If the image is on removable media, copy it to and run it from the swap file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_NET_RUN_FROM_SWAP"></a><a id="image_file_net_run_from_swap"></a><dl>
<dt><b>IMAGE_FILE_NET_RUN_FROM_SWAP</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
If the image is on the network, copy it to and run it from the swap file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_SYSTEM"></a><a id="image_file_system"></a><dl>
<dt><b>IMAGE_FILE_SYSTEM</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
The image is a system file.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_DLL"></a><a id="image_file_dll"></a><dl>
<dt><b>IMAGE_FILE_DLL</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
The image is a DLL file. While it is an executable file, it cannot be run directly.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_UP_SYSTEM_ONLY"></a><a id="image_file_up_system_only"></a><dl>
<dt><b>IMAGE_FILE_UP_SYSTEM_ONLY</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
The file should be run only on a uniprocessor computer.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_FILE_BYTES_REVERSED_HI"></a><a id="image_file_bytes_reversed_hi"></a><dl>
<dt><b>IMAGE_FILE_BYTES_REVERSED_HI</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
The bytes of the word are reversed. This flag is obsolete.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a>



<a href="/windows/desktop/Debug/imagehlp-structures">ImageHlp Structures</a>
