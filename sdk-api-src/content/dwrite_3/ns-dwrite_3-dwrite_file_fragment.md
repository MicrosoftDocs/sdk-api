---
UID: NS:dwrite_3.DWRITE_FILE_FRAGMENT
title: DWRITE_FILE_FRAGMENT (dwrite_3.h)
description: Represents a range of bytes in a font file.
helpviewer_keywords: ["DWRITE_FILE_FRAGMENT","DWRITE_FILE_FRAGMENT structure [Direct Write]","directwrite.dwrite_file_fragment","dwrite_3/DWRITE_FILE_FRAGMENT"]
old-location: directwrite\dwrite_file_fragment.htm
tech.root: DirectWrite
ms.assetid: 6E893719-E2A7-482A-B344-8FE2AA59A6B9
ms.date: 09/10/2025
ms.keywords: DWRITE_FILE_FRAGMENT, DWRITE_FILE_FRAGMENT structure [Direct Write], directwrite.dwrite_file_fragment, dwrite_3/DWRITE_FILE_FRAGMENT
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 15063
req.target-min-winversvr: Windows 10 Build 15063
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DWRITE_FILE_FRAGMENT
 - dwrite_3/DWRITE_FILE_FRAGMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_FILE_FRAGMENT
---

# DWRITE_FILE_FRAGMENT structure


## -description

Represents a range of bytes in a font file.

## -struct-fields

### -field fileOffset

Starting offset of the fragment from the beginning of the file.

### -field fragmentSize

Size of the file fragment, in bytes.

## -remarks

DWRITE_FILE_FRAGMENT is passed as input to <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteremotefontfilestream-begindownload">IDWriteRemoteFontFileStream::BeginDownload</a>.

