---
UID: NS:winnt._IMAGE_OPTIONAL_HEADER
title: IMAGE_OPTIONAL_HEADER32 (winnt.h)
description: Represents the optional header format. (32 bit)
helpviewer_keywords: ["*PIMAGE_OPTIONAL_HEADER32","IMAGE_DLLCHARACTERISTICS_DYNAMIC_BASE","IMAGE_DLLCHARACTERISTICS_FORCE_INTEGRITY","IMAGE_DLLCHARACTERISTICS_NO_BIND","IMAGE_DLLCHARACTERISTICS_NO_ISOLATION","IMAGE_DLLCHARACTERISTICS_NO_SEH","IMAGE_DLLCHARACTERISTICS_NX_COMPAT","IMAGE_DLLCHARACTERISTICS_TERMINAL_SERVER_AWARE","IMAGE_DLLCHARACTERISTICS_WDM_DRIVER","IMAGE_NT_OPTIONAL_HDR32_MAGIC","IMAGE_NT_OPTIONAL_HDR64_MAGIC","IMAGE_NT_OPTIONAL_HDR_MAGIC","IMAGE_OPTIONAL_HEADER","IMAGE_OPTIONAL_HEADER structure","IMAGE_OPTIONAL_HEADER32","IMAGE_OPTIONAL_HEADER64","IMAGE_ROM_OPTIONAL_HDR_MAGIC","IMAGE_SUBSYSTEM_EFI_APPLICATION","IMAGE_SUBSYSTEM_EFI_BOOT_SERVICE_DRIVER","IMAGE_SUBSYSTEM_EFI_ROM","IMAGE_SUBSYSTEM_EFI_RUNTIME_DRIVER","IMAGE_SUBSYSTEM_NATIVE","IMAGE_SUBSYSTEM_OS2_CUI","IMAGE_SUBSYSTEM_POSIX_CUI","IMAGE_SUBSYSTEM_UNKNOWN","IMAGE_SUBSYSTEM_WINDOWS_BOOT_APPLICATION","IMAGE_SUBSYSTEM_WINDOWS_CE_GUI","IMAGE_SUBSYSTEM_WINDOWS_CUI","IMAGE_SUBSYSTEM_WINDOWS_GUI","IMAGE_SUBSYSTEM_XBOX","PIMAGE_OPTIONAL_HEADER","PIMAGE_OPTIONAL_HEADER structure pointer","PIMAGE_OPTIONAL_HEADER32","PIMAGE_OPTIONAL_HEADER64","_IMAGE_OPTIONAL_HEADER","_win32_image_optional_header_str","base.image_optional_header_str","winnt/IMAGE_OPTIONAL_HEADER","winnt/PIMAGE_OPTIONAL_HEADER"]
old-location: base\image_optional_header_str.htm
tech.root: Debug
ms.assetid: b6a50ffc-49f8-4824-9b51-7e381eaf8852
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_OPTIONAL_HEADER32, IMAGE_DLLCHARACTERISTICS_DYNAMIC_BASE, IMAGE_DLLCHARACTERISTICS_FORCE_INTEGRITY, IMAGE_DLLCHARACTERISTICS_NO_BIND, IMAGE_DLLCHARACTERISTICS_NO_ISOLATION, IMAGE_DLLCHARACTERISTICS_NO_SEH, IMAGE_DLLCHARACTERISTICS_NX_COMPAT, IMAGE_DLLCHARACTERISTICS_TERMINAL_SERVER_AWARE, IMAGE_DLLCHARACTERISTICS_WDM_DRIVER, IMAGE_NT_OPTIONAL_HDR32_MAGIC, IMAGE_NT_OPTIONAL_HDR64_MAGIC, IMAGE_NT_OPTIONAL_HDR_MAGIC, IMAGE_OPTIONAL_HEADER, IMAGE_OPTIONAL_HEADER structure, IMAGE_OPTIONAL_HEADER32, IMAGE_OPTIONAL_HEADER64, IMAGE_ROM_OPTIONAL_HDR_MAGIC, IMAGE_SUBSYSTEM_EFI_APPLICATION, IMAGE_SUBSYSTEM_EFI_BOOT_SERVICE_DRIVER, IMAGE_SUBSYSTEM_EFI_ROM, IMAGE_SUBSYSTEM_EFI_RUNTIME_DRIVER, IMAGE_SUBSYSTEM_NATIVE, IMAGE_SUBSYSTEM_OS2_CUI, IMAGE_SUBSYSTEM_POSIX_CUI, IMAGE_SUBSYSTEM_UNKNOWN, IMAGE_SUBSYSTEM_WINDOWS_BOOT_APPLICATION, IMAGE_SUBSYSTEM_WINDOWS_CE_GUI, IMAGE_SUBSYSTEM_WINDOWS_CUI, IMAGE_SUBSYSTEM_WINDOWS_GUI, IMAGE_SUBSYSTEM_XBOX, PIMAGE_OPTIONAL_HEADER, PIMAGE_OPTIONAL_HEADER structure pointer, PIMAGE_OPTIONAL_HEADER32, PIMAGE_OPTIONAL_HEADER64, _IMAGE_OPTIONAL_HEADER, _win32_image_optional_header_str, base.image_optional_header_str, winnt/IMAGE_OPTIONAL_HEADER, winnt/PIMAGE_OPTIONAL_HEADER'
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
req.typenames: IMAGE_OPTIONAL_HEADER32, *PIMAGE_OPTIONAL_HEADER32
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_OPTIONAL_HEADER
 - winnt/_IMAGE_OPTIONAL_HEADER
 - PIMAGE_OPTIONAL_HEADER32
 - winnt/PIMAGE_OPTIONAL_HEADER32
 - IMAGE_OPTIONAL_HEADER32
 - winnt/IMAGE_OPTIONAL_HEADER32
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
 - IMAGE_OPTIONAL_HEADER
 - IMAGE_OPTIONAL_HEADER32
 - PIMAGE_OPTIONAL_HEADER32
 - IMAGE_OPTIONAL_HEADER64
 - PIMAGE_OPTIONAL_HEADER64
---

# IMAGE_OPTIONAL_HEADER32 structure


## -description

Represents the optional header format.

## -struct-fields

### -field Magic

The state of the image file. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_NT_OPTIONAL_HDR_MAGIC"></a><a id="image_nt_optional_hdr_magic"></a><dl>
<dt><b>IMAGE_NT_OPTIONAL_HDR_MAGIC</b></dt>
</dl>
</td>
<td width="60%">
The file is an executable image. This value is defined as 
        <b>IMAGE_NT_OPTIONAL_HDR32_MAGIC</b> in a 32-bit application and as 
        <b>IMAGE_NT_OPTIONAL_HDR64_MAGIC</b> in a 64-bit application.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_NT_OPTIONAL_HDR32_MAGIC"></a><a id="image_nt_optional_hdr32_magic"></a><dl>
<dt><b>IMAGE_NT_OPTIONAL_HDR32_MAGIC</b></dt>
<dt>0x10b</dt>
</dl>
</td>
<td width="60%">
The file is an executable image.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_NT_OPTIONAL_HDR64_MAGIC"></a><a id="image_nt_optional_hdr64_magic"></a><dl>
<dt><b>IMAGE_NT_OPTIONAL_HDR64_MAGIC</b></dt>
<dt>0x20b</dt>
</dl>
</td>
<td width="60%">
The file is an executable image.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_ROM_OPTIONAL_HDR_MAGIC"></a><a id="image_rom_optional_hdr_magic"></a><dl>
<dt><b>IMAGE_ROM_OPTIONAL_HDR_MAGIC</b></dt>
<dt>0x107</dt>
</dl>
</td>
<td width="60%">
The file is a ROM image.

</td>
</tr>
</table>

### -field MajorLinkerVersion

The major version number of the linker.

### -field MinorLinkerVersion

The minor version number of the linker.

### -field SizeOfCode

The size of the code section, in bytes, or the sum of all such sections if there are multiple code 
      sections.

### -field SizeOfInitializedData

The size of the initialized data section, in bytes, or the sum of all such sections if there are multiple 
      initialized data sections.

### -field SizeOfUninitializedData

The size of the uninitialized data section, in bytes, or the sum of all such sections if there are multiple 
      uninitialized data sections.

### -field AddressOfEntryPoint

A pointer to the entry point function, relative to the image base address. For executable files, this is 
      the starting address. For device drivers, this is the address of the initialization function. The entry point 
      function is optional for DLLs. When no entry point is present, this member is zero.

### -field BaseOfCode

A pointer to the beginning of the code section, relative to the image base.

### -field BaseOfData

A pointer to the beginning of the data section, relative to the image base.

### -field ImageBase

The preferred address of the first byte of the image when it is loaded in memory. This value is a multiple 
      of 64K bytes. The default value for DLLs is 0x10000000. The default value for applications is 0x00400000, except 
      on Windows CE where it is 0x00010000.

### -field SectionAlignment

The alignment of sections loaded in memory, in bytes. This value must be greater than or equal to the 
      <b>FileAlignment</b> member. The default value is the page size for the system.

### -field FileAlignment

The alignment of the raw data of sections in the image file, in bytes. The value should be a power of 2 
      between 512 and 64K (inclusive). The default is 512. If the <b>SectionAlignment</b> member 
      is less than the system page size, this member must be the same as 
      <b>SectionAlignment</b>.

### -field MajorOperatingSystemVersion

The major version number of the required operating system.

### -field MinorOperatingSystemVersion

The minor version number of the required operating system.

### -field MajorImageVersion

The major version number of the image.

### -field MinorImageVersion

The minor version number of the image.

### -field MajorSubsystemVersion

The major version number of the subsystem.

### -field MinorSubsystemVersion

The minor version number of the subsystem.

### -field Win32VersionValue

This member is reserved and must be 0.

### -field SizeOfImage

The size of the image, in bytes, including all headers. Must be a multiple of 
      <b>SectionAlignment</b>.

### -field SizeOfHeaders

The combined size of the following items, rounded to a multiple of the value specified in the 
      <b>FileAlignment</b> member.
      

<ul>
<li><b>e_lfanew</b> member of <b>IMAGE_DOS_HEADER</b></li>
<li>4 byte signature</li>
<li>size of <a href="/windows/desktop/api/winnt/ns-winnt-image_file_header">IMAGE_FILE_HEADER</a>
</li>
<li>size of optional header</li>
<li>size of all section headers</li>
</ul>

### -field CheckSum

The image file checksum. The following files are validated at load time: all drivers, any DLL loaded at 
      boot time, and any DLL loaded into a critical system process.

### -field Subsystem

The subsystem required to run this image. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_UNKNOWN"></a><a id="image_subsystem_unknown"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_UNKNOWN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Unknown subsystem.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_NATIVE"></a><a id="image_subsystem_native"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_NATIVE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
No subsystem required (device drivers and native system processes).

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_WINDOWS_GUI"></a><a id="image_subsystem_windows_gui"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_WINDOWS_GUI</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Windows graphical user interface (GUI) subsystem.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_WINDOWS_CUI"></a><a id="image_subsystem_windows_cui"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_WINDOWS_CUI</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Windows character-mode user interface (CUI) subsystem.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_OS2_CUI"></a><a id="image_subsystem_os2_cui"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_OS2_CUI</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
OS/2 CUI subsystem.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_POSIX_CUI"></a><a id="image_subsystem_posix_cui"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_POSIX_CUI</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
POSIX CUI subsystem.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_WINDOWS_CE_GUI"></a><a id="image_subsystem_windows_ce_gui"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_WINDOWS_CE_GUI</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Windows CE system.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_EFI_APPLICATION"></a><a id="image_subsystem_efi_application"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_EFI_APPLICATION</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Extensible Firmware Interface (EFI) application.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_EFI_BOOT_SERVICE_DRIVER"></a><a id="image_subsystem_efi_boot_service_driver"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_EFI_BOOT_SERVICE_DRIVER</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
EFI driver with boot services.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_EFI_RUNTIME_DRIVER"></a><a id="image_subsystem_efi_runtime_driver"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_EFI_RUNTIME_DRIVER</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
EFI driver with run-time services.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_EFI_ROM"></a><a id="image_subsystem_efi_rom"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_EFI_ROM</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
EFI ROM image.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_XBOX"></a><a id="image_subsystem_xbox"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_XBOX</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
Xbox system.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_SUBSYSTEM_WINDOWS_BOOT_APPLICATION"></a><a id="image_subsystem_windows_boot_application"></a><dl>
<dt><b>IMAGE_SUBSYSTEM_WINDOWS_BOOT_APPLICATION</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
Boot application.

</td>
</tr>
</table>

### -field DllCharacteristics

The DLL characteristics of the image. The following values are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLL_CHARACTERISTICS_HIGH_ENTROPY_VA"></a><a id="image_dll_characteristics_high_entropy_va"></a><dl>
<dt><b>IMAGE_DLL_CHARACTERISTICS_HIGH_ENTROPY_VA</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
ASLR with 64 bit address space.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLLCHARACTERISTICS_DYNAMIC_BASE"></a><a id="image_dllcharacteristics_dynamic_base"></a><dl>
<dt><b>IMAGE_DLLCHARACTERISTICS_DYNAMIC_BASE</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
The DLL can be relocated at load time.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLLCHARACTERISTICS_FORCE_INTEGRITY"></a><a id="image_dllcharacteristics_force_integrity"></a><dl>
<dt><b>IMAGE_DLLCHARACTERISTICS_FORCE_INTEGRITY</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Code integrity checks are forced. If you set this flag and a section contains only uninitialized data, 
        set the <b>PointerToRawData</b> member of 
        <a href="/windows/desktop/api/winnt/ns-winnt-image_section_header">IMAGE_SECTION_HEADER</a> for that section to 
        zero; otherwise, the image will fail to load because the digital signature cannot be verified.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLLCHARACTERISTICS_NX_COMPAT"></a><a id="image_dllcharacteristics_nx_compat"></a><dl>
<dt><b>IMAGE_DLLCHARACTERISTICS_NX_COMPAT</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
The image is compatible with data execution prevention (DEP).

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLLCHARACTERISTICS_NO_ISOLATION"></a><a id="image_dllcharacteristics_no_isolation"></a><dl>
<dt><b>IMAGE_DLLCHARACTERISTICS_NO_ISOLATION</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
The image is isolation aware, but should not be isolated.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLLCHARACTERISTICS_NO_SEH"></a><a id="image_dllcharacteristics_no_seh"></a><dl>
<dt><b>IMAGE_DLLCHARACTERISTICS_NO_SEH</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
The image does not use structured exception handling (SEH). No handlers can be called in this 
        image.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLLCHARACTERISTICS_NO_BIND"></a><a id="image_dllcharacteristics_no_bind"></a><dl>
<dt><b>IMAGE_DLLCHARACTERISTICS_NO_BIND</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
Do not bind the image.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLL_CHARACTERISTICS_APPCONTAINER"></a><a id="image_dll_characteristics_appcontainer"></a><dl>
<dt><b>IMAGE_DLL_CHARACTERISTICS_APPCONTAINER</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Image should execute in an AppContainer.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLLCHARACTERISTICS_WDM_DRIVER"></a><a id="image_dllcharacteristics_wdm_driver"></a><dl>
<dt><b>IMAGE_DLLCHARACTERISTICS_WDM_DRIVER</b></dt>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
A WDM driver.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLL_CHARACTERISTICS_GUARD_CF"></a><a id="image_dll_characteristics_guard_cf"></a><dl>
<dt><b>IMAGE_DLL_CHARACTERISTICS_GUARD_CF</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
Image supports Control Flow Guard.

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DLLCHARACTERISTICS_TERMINAL_SERVER_AWARE"></a><a id="image_dllcharacteristics_terminal_server_aware"></a><dl>
<dt><b>IMAGE_DLLCHARACTERISTICS_TERMINAL_SERVER_AWARE</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
The image is terminal server aware.

</td>
</tr>
</table>

### -field SizeOfStackReserve

The number of bytes to reserve for the stack. Only the memory specified by the 
      <b>SizeOfStackCommit</b> member is committed at load time; the rest is made available one 
      page at a time until this reserve size is reached.

### -field SizeOfStackCommit

The number of bytes to commit for the stack.

### -field SizeOfHeapReserve

The number of bytes to reserve for the local heap. Only the memory specified by the 
      <b>SizeOfHeapCommit</b> member is committed at load time; the rest is made available one 
      page at a time until this reserve size is reached.

### -field SizeOfHeapCommit

The number of bytes to commit for the local heap.

### -field LoaderFlags

This member is obsolete.

### -field NumberOfRvaAndSizes

The number of directory entries in the remainder of the optional header. Each entry describes a location 
      and size.

### -field DataDirectory

A pointer to the first 
<a href="/windows/desktop/api/winnt/ns-winnt-image_data_directory">IMAGE_DATA_DIRECTORY</a> structure in the data 
 directory.

The index number of the desired directory entry. This parameter can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_ARCHITECTURE"></a><a id="image_directory_entry_architecture"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_ARCHITECTURE</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Architecture-specific data

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_BASERELOC"></a><a id="image_directory_entry_basereloc"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_BASERELOC</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Base relocation table

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_BOUND_IMPORT"></a><a id="image_directory_entry_bound_import"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_BOUND_IMPORT</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Bound import directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_COM_DESCRIPTOR"></a><a id="image_directory_entry_com_descriptor"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_COM_DESCRIPTOR</b></dt>
<dt>14</dt>
</dl>
</td>
<td width="60%">
COM descriptor table

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_DEBUG"></a><a id="image_directory_entry_debug"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_DEBUG</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Debug directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_DELAY_IMPORT"></a><a id="image_directory_entry_delay_import"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_DELAY_IMPORT</b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
Delay import table

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_EXCEPTION"></a><a id="image_directory_entry_exception"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_EXCEPTION</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Exception directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_EXPORT"></a><a id="image_directory_entry_export"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_EXPORT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Export directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_GLOBALPTR"></a><a id="image_directory_entry_globalptr"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_GLOBALPTR</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The relative virtual address of global pointer

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_IAT"></a><a id="image_directory_entry_iat"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_IAT</b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
Import address table

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_IMPORT"></a><a id="image_directory_entry_import"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_IMPORT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Import directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_LOAD_CONFIG"></a><a id="image_directory_entry_load_config"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_LOAD_CONFIG</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
Load configuration directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_RESOURCE"></a><a id="image_directory_entry_resource"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_RESOURCE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Resource directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_SECURITY"></a><a id="image_directory_entry_security"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_SECURITY</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Security directory

</td>
</tr>
<tr>
<td width="40%"><a id="IMAGE_DIRECTORY_ENTRY_TLS"></a><a id="image_directory_entry_tls"></a><dl>
<dt><b>IMAGE_DIRECTORY_ENTRY_TLS</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Thread local storage directory

</td>
</tr>
</table>

## -remarks

The number of directories is not fixed. Check the <b>NumberOfRvaAndSizes</b> member before 
    looking for a specific directory.

The actual structure in WinNT.h is named <b>IMAGE_OPTIONAL_HEADER32</b> 
   and <b>IMAGE_OPTIONAL_HEADER</b> is defined as 
   <b>IMAGE_OPTIONAL_HEADER32</b>. However, if <b>_WIN64</b> is 
   defined, then <b>IMAGE_OPTIONAL_HEADER</b> is defined as 
   <b>IMAGE_OPTIONAL_HEADER64</b>.
   


```cpp
typedef struct _IMAGE_OPTIONAL_HEADER64 {
 WORD        Magic;
 BYTE        MajorLinkerVersion;
 BYTE        MinorLinkerVersion;
 DWORD       SizeOfCode;
 DWORD       SizeOfInitializedData;
 DWORD       SizeOfUninitializedData;
 DWORD       AddressOfEntryPoint;
 DWORD       BaseOfCode;
 ULONGLONG   ImageBase;
 DWORD       SectionAlignment;
 DWORD       FileAlignment;
 WORD        MajorOperatingSystemVersion;
 WORD        MinorOperatingSystemVersion;
 WORD        MajorImageVersion;
 WORD        MinorImageVersion;
 WORD        MajorSubsystemVersion;
 WORD        MinorSubsystemVersion;
 DWORD       Win32VersionValue;
 DWORD       SizeOfImage;
 DWORD       SizeOfHeaders;
 DWORD       CheckSum;
 WORD        Subsystem;
 WORD        DllCharacteristics;
 ULONGLONG   SizeOfStackReserve;
 ULONGLONG   SizeOfStackCommit;
 ULONGLONG   SizeOfHeapReserve;
 ULONGLONG   SizeOfHeapCommit;
 DWORD       LoaderFlags;
 DWORD       NumberOfRvaAndSizes;
 IMAGE_DATA_DIRECTORY DataDirectory[IMAGE_NUMBEROF_DIRECTORY_ENTRIES];
} IMAGE_OPTIONAL_HEADER64, *PIMAGE_OPTIONAL_HEADER64;
```

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-image_data_directory">IMAGE_DATA_DIRECTORY</a>



<a href="/windows/desktop/Debug/imagehlp-structures">ImageHlp Structures</a>
