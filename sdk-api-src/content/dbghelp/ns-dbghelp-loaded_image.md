---
UID: NS:dbghelp._LOADED_IMAGE
title: LOADED_IMAGE (dbghelp.h)
description: Contains information about the loaded image.
helpviewer_keywords: ["*PLOADED_IMAGE","IMAGE_FILE_32BIT_MACHINE","IMAGE_FILE_AGGRESIVE_WS_TRIM","IMAGE_FILE_BYTES_REVERSED_HI","IMAGE_FILE_BYTES_REVERSED_LO","IMAGE_FILE_DEBUG_STRIPPED","IMAGE_FILE_DLL","IMAGE_FILE_EXECUTABLE_IMAGE","IMAGE_FILE_LARGE_ADDRESS_AWARE","IMAGE_FILE_LINE_NUMS_STRIPPED","IMAGE_FILE_LOCAL_SYMS_STRIPPED","IMAGE_FILE_NET_RUN_FROM_SWAP","IMAGE_FILE_RELOCS_STRIPPED","IMAGE_FILE_REMOVABLE_RUN_FROM_SWAP","IMAGE_FILE_SYSTEM","IMAGE_FILE_UP_SYSTEM_ONLY","LOADED_IMAGE","LOADED_IMAGE structure","PLOADED_IMAGE","PLOADED_IMAGE structure pointer","_win32_loaded_image_str","base.loaded_image_str","dbghelp/LOADED_IMAGE","dbghelp/PLOADED_IMAGE"]
old-location: base\loaded_image_str.htm
tech.root: Debug
ms.assetid: 8bfc6b47-23d6-45e1-a733-5b938d6312da
ms.date: 12/05/2018
ms.keywords: '*PLOADED_IMAGE, IMAGE_FILE_32BIT_MACHINE, IMAGE_FILE_AGGRESIVE_WS_TRIM, IMAGE_FILE_BYTES_REVERSED_HI, IMAGE_FILE_BYTES_REVERSED_LO, IMAGE_FILE_DEBUG_STRIPPED, IMAGE_FILE_DLL, IMAGE_FILE_EXECUTABLE_IMAGE, IMAGE_FILE_LARGE_ADDRESS_AWARE, IMAGE_FILE_LINE_NUMS_STRIPPED, IMAGE_FILE_LOCAL_SYMS_STRIPPED, IMAGE_FILE_NET_RUN_FROM_SWAP, IMAGE_FILE_RELOCS_STRIPPED, IMAGE_FILE_REMOVABLE_RUN_FROM_SWAP, IMAGE_FILE_SYSTEM, IMAGE_FILE_UP_SYSTEM_ONLY, LOADED_IMAGE, LOADED_IMAGE structure, PLOADED_IMAGE, PLOADED_IMAGE structure pointer, _win32_loaded_image_str, base.loaded_image_str, dbghelp/LOADED_IMAGE, dbghelp/PLOADED_IMAGE'
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
targetos: Windows
req.typenames: LOADED_IMAGE, *PLOADED_IMAGE
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _LOADED_IMAGE
 - dbghelp/_LOADED_IMAGE
 - PLOADED_IMAGE
 - dbghelp/PLOADED_IMAGE
 - LOADED_IMAGE
 - dbghelp/LOADED_IMAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - LOADED_IMAGE
---

# LOADED_IMAGE structure


## -description

Contains information about the loaded image.

## -struct-fields

### -field ModuleName

The file name of the mapped file.

### -field hFile

A handle to the mapped file.

### -field MappedAddress

The base address of the mapped file.

### -field FileHeader

A pointer to an 
<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a> structure.

### -field LastRvaSection

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-image_section_header">IMAGE_SECTION_HEADER</a> structure.

### -field NumberOfSections

The number of COFF section headers.

### -field Sections

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-image_section_header">IMAGE_SECTION_HEADER</a> structure.

### -field Characteristics

The image characteristics value. This member can be one of the following values.

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
Bytes of word are reversed.

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

### -field fSystemImage

If the image is a kernel mode executable image, this value is <b>TRUE</b>.

### -field fDOSImage

If the image is a 16-bit executable image, this value is <b>TRUE</b>.

### -field fReadOnly

If the image is read-only, this value is <b>TRUE</b>.

<b>Prior to Windows Vista:  </b>This member is not included in the structure.

### -field Version

The version string.

<b>Prior to Windows Vista:  </b>This member is not included in the structure.

### -field Links

The list of loaded images.

### -field SizeOfImage

The size of the image, in bytes.

## -remarks

The <b>LIST_ENTRY</b> structure is defined as follows:


```cpp
typedef struct _LIST_ENTRY {
   struct _LIST_ENTRY *Flink;
   struct _LIST_ENTRY *Blink;
} LIST_ENTRY, *PLIST_ENTRY, *RESTRICTED_POINTER PRLIST_ENTRY;
```

## -see-also

<a href="/windows/win32/api/winnt/ns-winnt-image_nt_headers32">IMAGE_NT_HEADERS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-image_section_header">IMAGE_SECTION_HEADER</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-imageload">ImageLoad</a>



<a href="/windows/desktop/api/imagehlp/nf-imagehlp-mapandload">MapAndLoad</a>