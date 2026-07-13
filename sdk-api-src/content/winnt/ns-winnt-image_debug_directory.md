---
UID: NS:winnt._IMAGE_DEBUG_DIRECTORY
title: IMAGE_DEBUG_DIRECTORY (winnt.h)
description: Represents the debug directory format.
helpviewer_keywords: ["*PIMAGE_DEBUG_DIRECTORY","IMAGE_DEBUG_DIRECTORY","IMAGE_DEBUG_DIRECTORY structure","IMAGE_DEBUG_TYPE_BORLAND","IMAGE_DEBUG_TYPE_CODEVIEW","IMAGE_DEBUG_TYPE_COFF","IMAGE_DEBUG_TYPE_EXCEPTION","IMAGE_DEBUG_TYPE_FIXUP","IMAGE_DEBUG_TYPE_FPO","IMAGE_DEBUG_TYPE_MISC","IMAGE_DEBUG_TYPE_UNKNOWN","PIMAGE_DEBUG_DIRECTORY","PIMAGE_DEBUG_DIRECTORY structure pointer","_IMAGE_DEBUG_DIRECTORY","_win32_image_debug_directory_str","base.image_debug_directory_str","winnt/IMAGE_DEBUG_DIRECTORY","winnt/PIMAGE_DEBUG_DIRECTORY"]
old-location: base\image_debug_directory_str.htm
tech.root: Debug
ms.assetid: f89a3c9b-4d73-4ff5-8f45-2e58500d5084
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_DEBUG_DIRECTORY, IMAGE_DEBUG_DIRECTORY, IMAGE_DEBUG_DIRECTORY structure, IMAGE_DEBUG_TYPE_BORLAND, IMAGE_DEBUG_TYPE_CODEVIEW, IMAGE_DEBUG_TYPE_COFF, IMAGE_DEBUG_TYPE_EXCEPTION, IMAGE_DEBUG_TYPE_FIXUP, IMAGE_DEBUG_TYPE_FPO, IMAGE_DEBUG_TYPE_MISC, IMAGE_DEBUG_TYPE_UNKNOWN, PIMAGE_DEBUG_DIRECTORY, PIMAGE_DEBUG_DIRECTORY structure pointer, _IMAGE_DEBUG_DIRECTORY, _win32_image_debug_directory_str, base.image_debug_directory_str, winnt/IMAGE_DEBUG_DIRECTORY, winnt/PIMAGE_DEBUG_DIRECTORY'
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
req.typenames: IMAGE_DEBUG_DIRECTORY, *PIMAGE_DEBUG_DIRECTORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_DEBUG_DIRECTORY
 - winnt/_IMAGE_DEBUG_DIRECTORY
 - PIMAGE_DEBUG_DIRECTORY
 - winnt/PIMAGE_DEBUG_DIRECTORY
 - IMAGE_DEBUG_DIRECTORY
 - winnt/IMAGE_DEBUG_DIRECTORY
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
 - IMAGE_DEBUG_DIRECTORY
---

# IMAGE_DEBUG_DIRECTORY structure


## -description

Represents the debug directory format.

## -struct-fields

### -field Characteristics

Reserved.

### -field TimeDateStamp

The time and date the debugging information was created.

### -field MajorVersion

The major version number of the debugging information format.

### -field MinorVersion

The minor version number of the debugging information format.

### -field Type

The format of debugging information. This field enables support of multiple debuggers. For more information, see [Debug Type](/windows/win32/debug/pe-format#debug-type) in PE Format specification.

### -field SizeOfData

The size of the debugging information, in bytes. This value does not include the debug directory itself.

### -field AddressOfRawData

The address of the debugging information when the image is loaded, relative to the image base.

### -field PointerToRawData

A file pointer to the debugging information.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-structures">ImageHlp Structures</a>
