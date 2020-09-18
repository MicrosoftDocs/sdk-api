---
UID: NS:winnt._IMAGE_SECTION_HEADER
title: IMAGE_SECTION_HEADER (winnt.h)
description: Represents the image section header format.
helpviewer_keywords: ["*PIMAGE_SECTION_HEADER","IMAGE_SCN_ALIGN_1024BYTES","IMAGE_SCN_ALIGN_128BYTES","IMAGE_SCN_ALIGN_16BYTES","IMAGE_SCN_ALIGN_1BYTES","IMAGE_SCN_ALIGN_2048BYTES","IMAGE_SCN_ALIGN_256BYTES","IMAGE_SCN_ALIGN_2BYTES","IMAGE_SCN_ALIGN_32BYTES","IMAGE_SCN_ALIGN_4096BYTES","IMAGE_SCN_ALIGN_4BYTES","IMAGE_SCN_ALIGN_512BYTES","IMAGE_SCN_ALIGN_64BYTES","IMAGE_SCN_ALIGN_8192BYTES","IMAGE_SCN_ALIGN_8BYTES","IMAGE_SCN_CNT_CODE","IMAGE_SCN_CNT_INITIALIZED_DATA","IMAGE_SCN_CNT_UNINITIALIZED_DATA","IMAGE_SCN_GPREL","IMAGE_SCN_LNK_COMDAT","IMAGE_SCN_LNK_INFO","IMAGE_SCN_LNK_NRELOC_OVFL","IMAGE_SCN_LNK_OTHER","IMAGE_SCN_LNK_REMOVE","IMAGE_SCN_MEM_DISCARDABLE","IMAGE_SCN_MEM_EXECUTE","IMAGE_SCN_MEM_LOCKED","IMAGE_SCN_MEM_NOT_CACHED","IMAGE_SCN_MEM_NOT_PAGED","IMAGE_SCN_MEM_PRELOAD","IMAGE_SCN_MEM_PURGEABLE","IMAGE_SCN_MEM_READ","IMAGE_SCN_MEM_SHARED","IMAGE_SCN_MEM_WRITE","IMAGE_SCN_NO_DEFER_SPEC_EXC","IMAGE_SCN_TYPE_NO_PAD","IMAGE_SECTION_HEADER","IMAGE_SECTION_HEADER structure","PIMAGE_SECTION_HEADER","PIMAGE_SECTION_HEADER structure pointer","_IMAGE_SECTION_HEADER","_win32_image_section_header_str","base.image_section_header_str","winnt/IMAGE_SECTION_HEADER","winnt/PIMAGE_SECTION_HEADER"]
old-location: base\image_section_header_str.htm
tech.root: Debug
ms.assetid: 81ddf56d-66cc-4a0c-9cff-a84376a3223d
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_SECTION_HEADER, IMAGE_SCN_ALIGN_1024BYTES, IMAGE_SCN_ALIGN_128BYTES, IMAGE_SCN_ALIGN_16BYTES, IMAGE_SCN_ALIGN_1BYTES, IMAGE_SCN_ALIGN_2048BYTES, IMAGE_SCN_ALIGN_256BYTES, IMAGE_SCN_ALIGN_2BYTES, IMAGE_SCN_ALIGN_32BYTES, IMAGE_SCN_ALIGN_4096BYTES, IMAGE_SCN_ALIGN_4BYTES, IMAGE_SCN_ALIGN_512BYTES, IMAGE_SCN_ALIGN_64BYTES, IMAGE_SCN_ALIGN_8192BYTES, IMAGE_SCN_ALIGN_8BYTES, IMAGE_SCN_CNT_CODE, IMAGE_SCN_CNT_INITIALIZED_DATA, IMAGE_SCN_CNT_UNINITIALIZED_DATA, IMAGE_SCN_GPREL, IMAGE_SCN_LNK_COMDAT, IMAGE_SCN_LNK_INFO, IMAGE_SCN_LNK_NRELOC_OVFL, IMAGE_SCN_LNK_OTHER, IMAGE_SCN_LNK_REMOVE, IMAGE_SCN_MEM_DISCARDABLE, IMAGE_SCN_MEM_EXECUTE, IMAGE_SCN_MEM_LOCKED, IMAGE_SCN_MEM_NOT_CACHED, IMAGE_SCN_MEM_NOT_PAGED, IMAGE_SCN_MEM_PRELOAD, IMAGE_SCN_MEM_PURGEABLE, IMAGE_SCN_MEM_READ, IMAGE_SCN_MEM_SHARED, IMAGE_SCN_MEM_WRITE, IMAGE_SCN_NO_DEFER_SPEC_EXC, IMAGE_SCN_TYPE_NO_PAD, IMAGE_SECTION_HEADER, IMAGE_SECTION_HEADER structure, PIMAGE_SECTION_HEADER, PIMAGE_SECTION_HEADER structure pointer, _IMAGE_SECTION_HEADER, _win32_image_section_header_str, base.image_section_header_str, winnt/IMAGE_SECTION_HEADER, winnt/PIMAGE_SECTION_HEADER'
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
req.typenames: IMAGE_SECTION_HEADER, *PIMAGE_SECTION_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_SECTION_HEADER
 - winnt/_IMAGE_SECTION_HEADER
 - PIMAGE_SECTION_HEADER
 - winnt/PIMAGE_SECTION_HEADER
 - IMAGE_SECTION_HEADER
 - winnt/IMAGE_SECTION_HEADER
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
 - IMAGE_SECTION_HEADER
---

# IMAGE_SECTION_HEADER structure


## -description

Represents the image section header format.

## -struct-fields

### -field Name

An 8-byte, null-padded UTF-8 string. There is no terminating null character if the string is exactly eight characters long. For longer names, this member contains a forward slash (/) followed by an ASCII representation of a decimal number that is an offset into the string table. Executable images do not use a string table and do not support section names longer than eight characters.

### -field Misc

### -field Misc.PhysicalAddress

The file address.

### -field Misc.VirtualSize

The total size of the section when loaded into memory, in bytes. If this value is greater than the <b>SizeOfRawData</b> member, the section is filled with zeroes. This field is valid only for executable images and should be set to 0 for object files.

### -field VirtualAddress

The address of the first byte of the section when loaded into memory, relative to the image base. For object files, this is the address of the first byte before relocation is applied.

### -field SizeOfRawData

The size of the initialized data on disk, in bytes. This value must be a multiple of the <b>FileAlignment</b> member of the 
<a href="/windows/win32/api/winnt/ns-winnt-image_optional_header32">IMAGE_OPTIONAL_HEADER</a> structure. If this value is less than the <b>VirtualSize</b> member, the remainder of the section is filled with zeroes. If the section contains only uninitialized data, the member is zero.

### -field PointerToRawData

A file pointer to the first page within the COFF file. This value must be a multiple of the <b>FileAlignment</b> member of the 
<a href="/windows/win32/api/winnt/ns-winnt-image_optional_header32">IMAGE_OPTIONAL_HEADER</a> structure. If a section contains only uninitialized data, set this member is zero.

### -field PointerToRelocations

 A file pointer to the beginning of the relocation entries for the section. If there are no relocations, this value is zero.

### -field PointerToLinenumbers

A file pointer to the beginning of the line-number entries for the section. If there are no COFF line numbers, this value is zero.

### -field NumberOfRelocations

The number of relocation entries for the section. This value is zero for executable images.

### -field NumberOfLinenumbers

The number of line-number entries for the section.

### -field Characteristics

The characteristics of the image. The following values are defined. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_TYPE_NO_PAD"></a><a id="image_scn_type_no_pad"></a><dl>
<dt><b>IMAGE_SCN_TYPE_NO_PAD</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The section should not be padded to the next boundary. This flag is obsolete and is replaced by IMAGE_SCN_ALIGN_1BYTES.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_CNT_CODE"></a><a id="image_scn_cnt_code"></a><dl>
<dt><b>IMAGE_SCN_CNT_CODE</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
The section contains executable code.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_CNT_INITIALIZED_DATA"></a><a id="image_scn_cnt_initialized_data"></a><dl>
<dt><b>IMAGE_SCN_CNT_INITIALIZED_DATA</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
The section contains initialized data.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_CNT_UNINITIALIZED_DATA"></a><a id="image_scn_cnt_uninitialized_data"></a><dl>
<dt><b>IMAGE_SCN_CNT_UNINITIALIZED_DATA</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
The section contains uninitialized data.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_LNK_OTHER"></a><a id="image_scn_lnk_other"></a><dl>
<dt><b>IMAGE_SCN_LNK_OTHER</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_LNK_INFO"></a><a id="image_scn_lnk_info"></a><dl>
<dt><b>IMAGE_SCN_LNK_INFO</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
The section contains comments or other information. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_LNK_REMOVE"></a><a id="image_scn_lnk_remove"></a><dl>
<dt><b>IMAGE_SCN_LNK_REMOVE</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
The section will not become part of the image. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_LNK_COMDAT"></a><a id="image_scn_lnk_comdat"></a><dl>
<dt><b>IMAGE_SCN_LNK_COMDAT</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The section contains COMDAT data. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_NO_DEFER_SPEC_EXC"></a><a id="image_scn_no_defer_spec_exc"></a><dl>
<dt><b>IMAGE_SCN_NO_DEFER_SPEC_EXC</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Reset speculative exceptions handling bits in the TLB entries for this section.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_GPREL"></a><a id="image_scn_gprel"></a><dl>
<dt><b>IMAGE_SCN_GPREL</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
The section contains data referenced through the global pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_PURGEABLE"></a><a id="image_scn_mem_purgeable"></a><dl>
<dt><b>IMAGE_SCN_MEM_PURGEABLE</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_LOCKED"></a><a id="image_scn_mem_locked"></a><dl>
<dt><b>IMAGE_SCN_MEM_LOCKED</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_PRELOAD"></a><a id="image_scn_mem_preload"></a><dl>
<dt><b>IMAGE_SCN_MEM_PRELOAD</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_1BYTES"></a><a id="image_scn_align_1bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_1BYTES</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Align data on a 1-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_2BYTES"></a><a id="image_scn_align_2bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_2BYTES</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
Align data on a 2-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_4BYTES"></a><a id="image_scn_align_4bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_4BYTES</b></dt>
<dt>0x00300000</dt>
</dl>
</td>
<td width="60%">
Align data on a 4-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_8BYTES"></a><a id="image_scn_align_8bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_8BYTES</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
Align data on a 8-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_16BYTES"></a><a id="image_scn_align_16bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_16BYTES</b></dt>
<dt>0x00500000</dt>
</dl>
</td>
<td width="60%">
Align data on a 16-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_32BYTES"></a><a id="image_scn_align_32bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_32BYTES</b></dt>
<dt>0x00600000</dt>
</dl>
</td>
<td width="60%">
Align data on a 32-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_64BYTES"></a><a id="image_scn_align_64bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_64BYTES</b></dt>
<dt>0x00700000</dt>
</dl>
</td>
<td width="60%">
Align data on a 64-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_128BYTES"></a><a id="image_scn_align_128bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_128BYTES</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
Align data on a 128-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_256BYTES"></a><a id="image_scn_align_256bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_256BYTES</b></dt>
<dt>0x00900000</dt>
</dl>
</td>
<td width="60%">
Align data on a 256-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_512BYTES"></a><a id="image_scn_align_512bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_512BYTES</b></dt>
<dt>0x00A00000</dt>
</dl>
</td>
<td width="60%">
Align data on a 512-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_1024BYTES"></a><a id="image_scn_align_1024bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_1024BYTES</b></dt>
<dt>0x00B00000</dt>
</dl>
</td>
<td width="60%">
Align data on a 1024-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_2048BYTES"></a><a id="image_scn_align_2048bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_2048BYTES</b></dt>
<dt>0x00C00000</dt>
</dl>
</td>
<td width="60%">
Align data on a 2048-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_4096BYTES"></a><a id="image_scn_align_4096bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_4096BYTES</b></dt>
<dt>0x00D00000</dt>
</dl>
</td>
<td width="60%">
Align data on a 4096-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_ALIGN_8192BYTES"></a><a id="image_scn_align_8192bytes"></a><dl>
<dt><b>IMAGE_SCN_ALIGN_8192BYTES</b></dt>
<dt>0x00E00000</dt>
</dl>
</td>
<td width="60%">
Align data on a 8192-byte boundary. This is valid only for object files.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_LNK_NRELOC_OVFL"></a><a id="image_scn_lnk_nreloc_ovfl"></a><dl>
<dt><b>IMAGE_SCN_LNK_NRELOC_OVFL</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
The section contains extended relocations. The count of relocations for the section exceeds the 16 bits that is reserved for it in the section header. If the <b>NumberOfRelocations</b> field in the section header is 0xffff, the actual relocation count is stored in the <b>VirtualAddress</b> field of the first relocation. It is an error if IMAGE_SCN_LNK_NRELOC_OVFL is set and there are fewer than 0xffff relocations in the section.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_DISCARDABLE"></a><a id="image_scn_mem_discardable"></a><dl>
<dt><b>IMAGE_SCN_MEM_DISCARDABLE</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
The section can be discarded as needed.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_NOT_CACHED"></a><a id="image_scn_mem_not_cached"></a><dl>
<dt><b>IMAGE_SCN_MEM_NOT_CACHED</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
The section cannot be cached.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_NOT_PAGED"></a><a id="image_scn_mem_not_paged"></a><dl>
<dt><b>IMAGE_SCN_MEM_NOT_PAGED</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
The section cannot be paged.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_SHARED"></a><a id="image_scn_mem_shared"></a><dl>
<dt><b>IMAGE_SCN_MEM_SHARED</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
The section can be shared in memory.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_EXECUTE"></a><a id="image_scn_mem_execute"></a><dl>
<dt><b>IMAGE_SCN_MEM_EXECUTE</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
The section can be executed as code.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_READ"></a><a id="image_scn_mem_read"></a><dl>
<dt><b>IMAGE_SCN_MEM_READ</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
The section can be read.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SCN_MEM_WRITE"></a><a id="image_scn_mem_write"></a><dl>
<dt><b>IMAGE_SCN_MEM_WRITE</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
The section can be written to.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagedirectoryentrytodataex">ImageDirectoryEntryToDataEx</a>



<a href="/windows/desktop/Debug/imagehlp-structures">ImageHlp Structures</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagervatosection">ImageRvaToSection</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-imagervatova">ImageRvaToVa</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image">LOADED_IMAGE</a>