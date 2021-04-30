---
UID: NS:minidumpapiset._MINIDUMP_HEADER
title: MINIDUMP_HEADER (minidumpapiset.h)
description: Contains header information for the minidump file.
helpviewer_keywords: ["*PMINIDUMP_HEADER","MINIDUMP_HEADER","MINIDUMP_HEADER structure","PMINIDUMP_HEADER","PMINIDUMP_HEADER structure pointer","_MINIDUMP_HEADER","_win32_minidump_header_str","base.minidump_header_str","minidumpapiset/MINIDUMP_HEADER","minidumpapiset/PMINIDUMP_HEADER"]
old-location: base\minidump_header_str.htm
tech.root: Debug
ms.assetid: 693bd569-e3f2-4cc7-b744-dd1f6da54736
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_HEADER, MINIDUMP_HEADER, MINIDUMP_HEADER structure, PMINIDUMP_HEADER, PMINIDUMP_HEADER structure pointer, _MINIDUMP_HEADER, _win32_minidump_header_str, base.minidump_header_str, minidumpapiset/MINIDUMP_HEADER, minidumpapiset/PMINIDUMP_HEADER'
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
req.typenames: MINIDUMP_HEADER, *PMINIDUMP_HEADER
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_HEADER
 - minidumpapiset/_MINIDUMP_HEADER
 - PMINIDUMP_HEADER
 - minidumpapiset/PMINIDUMP_HEADER
 - MINIDUMP_HEADER
 - minidumpapiset/MINIDUMP_HEADER
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
 - MINIDUMP_HEADER
---

# MINIDUMP_HEADER structure


## -description

Contains header information for the minidump file.

## -struct-fields

### -field Signature

The signature. Set this member to MINIDUMP_SIGNATURE.

### -field Version

The version of the minidump format. The low-order word is MINIDUMP_VERSION. The high-order word is an internal value that is implementation specific.

### -field NumberOfStreams

The number of streams in the minidump directory.

### -field StreamDirectoryRva

The base RVA of the minidump directory. The directory is an array of 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_directory">MINIDUMP_DIRECTORY</a> structures.

### -field CheckSum

The checksum for the minidump file. This member can be zero.

### -field Reserved

This member is reserved.

### -field TimeDateStamp

Time and date, in <b>time_t</b> format.

### -field Flags

One or more values from the 
<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type">MINIDUMP_TYPE</a> enumeration type.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_directory">MINIDUMP_DIRECTORY</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type">MINIDUMP_TYPE</a>