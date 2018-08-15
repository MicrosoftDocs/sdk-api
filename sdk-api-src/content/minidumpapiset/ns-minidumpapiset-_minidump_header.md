---
UID: NS:minidumpapiset._MINIDUMP_HEADER
title: "_MINIDUMP_HEADER"
author: windows-sdk-content
description: Contains header information for the minidump file.
old-location: base\minidump_header_str.htm
old-project: debug
ms.assetid: 693bd569-e3f2-4cc7-b744-dd1f6da54736
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMINIDUMP_HEADER, MINIDUMP_HEADER, MINIDUMP_HEADER structure, PMINIDUMP_HEADER, PMINIDUMP_HEADER structure pointer, _MINIDUMP_HEADER, _win32_minidump_header_str, base.minidump_header_str, minidumpapiset/MINIDUMP_HEADER, minidumpapiset/PMINIDUMP_HEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.redist: DbgHelp.dll 5.1 or later
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
tech.root: 
req.typenames: MINIDUMP_HEADER, *PMINIDUMP_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_HEADER structure


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
<a href="https://msdn.microsoft.com/1262c218-5351-4fea-9d35-4654da7c5e44">MINIDUMP_DIRECTORY</a> structures.


### -field CheckSum

The checksum for the minidump file. This member can be zero.


### -field Reserved

This member is reserved.


### -field TimeDateStamp

Time and date, in <b>time_t</b> format.


### -field Flags

One or more values from the 
<a href="https://msdn.microsoft.com/89ae3a75-5f02-4c5e-9d72-95fb8ef94985">MINIDUMP_TYPE</a> enumeration type.


## -see-also




<a href="https://msdn.microsoft.com/1262c218-5351-4fea-9d35-4654da7c5e44">MINIDUMP_DIRECTORY</a>



<a href="https://msdn.microsoft.com/89ae3a75-5f02-4c5e-9d72-95fb8ef94985">MINIDUMP_TYPE</a>
 

 

