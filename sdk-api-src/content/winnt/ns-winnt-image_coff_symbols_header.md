---
UID: NS:winnt._IMAGE_COFF_SYMBOLS_HEADER
title: IMAGE_COFF_SYMBOLS_HEADER (winnt.h)
description: Represents the COFF symbols header.
helpviewer_keywords: ["*PIMAGE_COFF_SYMBOLS_HEADER","IMAGE_COFF_SYMBOLS_HEADER","IMAGE_COFF_SYMBOLS_HEADER structure","PIMAGE_COFF_SYMBOLS_HEADER","PIMAGE_COFF_SYMBOLS_HEADER structure pointer","_IMAGE_COFF_SYMBOLS_HEADER","_win32_image_coff_symbols_header_str","base.image_coff_symbols_header_str","winnt/IMAGE_COFF_SYMBOLS_HEADER","winnt/PIMAGE_COFF_SYMBOLS_HEADER"]
old-location: base\image_coff_symbols_header_str.htm
tech.root: Debug
ms.assetid: f3a0ba0e-ef6b-4355-8dc4-5099dd54ab7e
ms.date: 12/05/2018
ms.keywords: '*PIMAGE_COFF_SYMBOLS_HEADER, IMAGE_COFF_SYMBOLS_HEADER, IMAGE_COFF_SYMBOLS_HEADER structure, PIMAGE_COFF_SYMBOLS_HEADER, PIMAGE_COFF_SYMBOLS_HEADER structure pointer, _IMAGE_COFF_SYMBOLS_HEADER, _win32_image_coff_symbols_header_str, base.image_coff_symbols_header_str, winnt/IMAGE_COFF_SYMBOLS_HEADER, winnt/PIMAGE_COFF_SYMBOLS_HEADER'
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
req.typenames: IMAGE_COFF_SYMBOLS_HEADER, *PIMAGE_COFF_SYMBOLS_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IMAGE_COFF_SYMBOLS_HEADER
 - winnt/_IMAGE_COFF_SYMBOLS_HEADER
 - PIMAGE_COFF_SYMBOLS_HEADER
 - winnt/PIMAGE_COFF_SYMBOLS_HEADER
 - IMAGE_COFF_SYMBOLS_HEADER
 - winnt/IMAGE_COFF_SYMBOLS_HEADER
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
 - IMAGE_COFF_SYMBOLS_HEADER
---

# IMAGE_COFF_SYMBOLS_HEADER structure


## -description

Represents the COFF symbols header.

## -struct-fields

### -field NumberOfSymbols

The number of symbols.

### -field LvaToFirstSymbol

The virtual address of the first symbol.

### -field NumberOfLinenumbers

The number of line-number entries.

### -field LvaToFirstLinenumber

The virtual address of the first line-number entry.

### -field RvaToFirstByteOfCode

The relative virtual address of the first byte of code.

### -field RvaToLastByteOfCode

The relative virtual address of the last byte of code.

### -field RvaToFirstByteOfData

The relative virtual address of the first byte of data.

### -field RvaToLastByteOfData

The relative virtual address of the last byte of data.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-structures">ImageHlp Structures</a>