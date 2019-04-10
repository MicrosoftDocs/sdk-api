---
UID: NE:compressapi.__unnamed_enum_0
title: COMPRESS_INFORMATION_CLASS (compressapi.h)
author: windows-sdk-content
description: The values of this enumeration identify the type of information class being set or retrieved.
old-location: cmpapi\compress_information_class.htm
tech.root: cmpapi
ms.assetid: ebdcbe03-b7fb-4dec-b906-086f8fe9be4c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: COMPRESS_INFORMATION_CLASS, COMPRESS_INFORMATION_CLASS enumeration [Compression API], COMPRESS_INFORMATION_CLASS_BLOCK_SIZE, COMPRESS_INFORMATION_CLASS_INVALID, COMPRESS_INFORMATION_CLASS_LEVEL, cmpapi.compress_information_class, compressapi/COMPRESS_INFORMATION_CLASS, compressapi/COMPRESS_INFORMATION_CLASS_BLOCK_SIZE, compressapi/COMPRESS_INFORMATION_CLASS_INVALID, compressapi/COMPRESS_INFORMATION_CLASS_LEVEL
ms.topic: enum
req.header: compressapi.h
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
 - compressapi.h
api_name:
 - COMPRESS_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: COMPRESS_INFORMATION_CLASS
req.redist: 
---

# COMPRESS_INFORMATION_CLASS enumeration


## -description


The values of this enumeration identify the type of information class being set or retrieved.


## -enum-fields




### -field COMPRESS_INFORMATION_CLASS_INVALID

Invalid information class


### -field COMPRESS_INFORMATION_CLASS_BLOCK_SIZE

Customized block size. The value specified may be from 65536 to 67108864 bytes. This value can be used only with the LZMS compression algorithm. A minimum size of 1 MB is suggested to get a better compression ratio. An information class of this type is sizeof(DWORD).


### -field COMPRESS_INFORMATION_CLASS_LEVEL

Desired level of compression. The default value is <b>(DWORD)0</b>. The value <b>(DWORD)1</b> can improve the compression ratio with a slightly slower compression speed. This value can be used only with the XPRESS compression algorithm or the XPRESS with Huffman encoding compression algorithm. An information class of this type is sizeof(DWORD).

