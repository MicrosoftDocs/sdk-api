---
UID: NS:processsnapshot.PSS_VA_SPACE_ENTRY
title: PSS_VA_SPACE_ENTRY (processsnapshot.h)
description: Holds the MEMORY_BASIC_INFORMATION returned by PssWalkSnapshot for a virtual address (VA) region.
helpviewer_keywords: ["PSS_VA_SPACE_ENTRY","PSS_VA_SPACE_ENTRY structure","proc_snap.pss_va_space_entry","processsnapshot/PSS_VA_SPACE_ENTRY"]
old-location: proc_snap\pss_va_space_entry.htm
tech.root: proc_snap
ms.assetid: 69B8F6A3-76DF-421B-B89B-73BA3254F897
ms.date: 12/05/2018
ms.keywords: PSS_VA_SPACE_ENTRY, PSS_VA_SPACE_ENTRY structure, proc_snap.pss_va_space_entry, processsnapshot/PSS_VA_SPACE_ENTRY
req.header: processsnapshot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: PSS_VA_SPACE_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSS_VA_SPACE_ENTRY
 - processsnapshot/PSS_VA_SPACE_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_VA_SPACE_ENTRY
---

# PSS_VA_SPACE_ENTRY structure


## -description

Holds the <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a> returned by <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a> for a virtual address (VA) region.

## -struct-fields

### -field BaseAddress

Information about the VA region. For more information, see <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a>.

### -field AllocationBase

Information about the VA region. For more information, see <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a>.

### -field AllocationProtect

Information about the VA region. For more information, see <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a>.

### -field RegionSize

Information about the VA region. For more information, see <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a>.

### -field State

Information about the VA region. For more information, see <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a>.

### -field Protect

Information about the VA region. For more information, see <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a>.

### -field Type

Information about the VA region. For more information, see <a href="/windows/desktop/api/winnt/ns-winnt-memory_basic_information">MEMORY_BASIC_INFORMATION</a>.

### -field TimeDateStamp

If section information was captured and the region is an executable image (<b>MEM_IMAGE</b>), this is the <b>TimeDateStamp</b> value from the Portable Executable (PE) header which describes the image. It is the low 32 bits of the number of seconds since 00:00 January 1, 1970 (a C run-time time_t value), that indicates when the file was created.

### -field SizeOfImage

If section information was captured and the region is an executable image (<b>MEM_IMAGE</b>), this is the <b>SizeOfImage</b> value from the Portable Executable (PE) header which describes the image. It is the size (in bytes) of the image, including all headers, as the image is loaded in memory.

### -field ImageBase

If section information was captured and the region is an executable image (<b>MEM_IMAGE</b>), this is the <b>ImageBase</b> value from the Portable Executable (PE) header which describes the image. It is the  preferred address of the first byte of the image when loaded into memory.

### -field CheckSum

If section information was captured and the region is an executable image (<b>MEM_IMAGE</b>), this is the <b>CheckSum</b> value from the Portable Executable (PE) header which describes the image. It is the image file checksum.

### -field MappedFileNameLength

The length of the mapped file name buffer, in bytes.

### -field MappedFileName

If section information was captured, this is the file path backing the section (if any). The path may be in NT namespace. The string may not be terminated by a <b>NULL</b> character. The pointer is valid for the lifetime of the walk marker passed to <a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a>.

## -remarks

<a href="/previous-versions/windows/desktop/api/processsnapshot/nf-processsnapshot-psswalksnapshot">PssWalkSnapshot</a> returns a <b>PSS_VA_SPACE_ENTRY</b> structure when the  <a href="/previous-versions/windows/desktop/api/processsnapshot/ne-processsnapshot-pss_walk_information_class">PSS_WALK_INFORMATION_CLASS</a> member that the caller provides it is <b>PSS_WALK_VA_SPACE</b>.

## -see-also

<a href="/previous-versions/windows/desktop/proc_snap/process-snapshotting-portal">Process Snapshotting</a>

