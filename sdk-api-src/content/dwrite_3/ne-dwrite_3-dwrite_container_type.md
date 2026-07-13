---
UID: NE:dwrite_3.DWRITE_CONTAINER_TYPE
title: DWRITE_CONTAINER_TYPE (dwrite_3.h)
description: Specifies the container format of a font resource. A container format is distinct from a font file format (DWRITE_FONT_FILE_TYPE) because the container describes the container in which the underlying font file is packaged.
helpviewer_keywords: ["DWRITE_CONTAINER_TYPE","DWRITE_CONTAINER_TYPE enumeration [Direct Write]","DWRITE_CONTAINER_TYPE_UNKNOWN","DWRITE_CONTAINER_TYPE_WOFF","DWRITE_CONTAINER_TYPE_WOFF2","directwrite.dwrite_container_type","dwrite_3/DWRITE_CONTAINER_TYPE","dwrite_3/DWRITE_CONTAINER_TYPE_UNKNOWN","dwrite_3/DWRITE_CONTAINER_TYPE_WOFF","dwrite_3/DWRITE_CONTAINER_TYPE_WOFF2"]
old-location: directwrite\dwrite_container_type.htm
tech.root: DirectWrite
ms.assetid: 93275F1D-A25C-4BDD-B278-DA56ADB3436D
ms.date: 09/10/2025
ms.keywords: DWRITE_CONTAINER_TYPE, DWRITE_CONTAINER_TYPE enumeration [Direct Write], DWRITE_CONTAINER_TYPE_UNKNOWN, DWRITE_CONTAINER_TYPE_WOFF, DWRITE_CONTAINER_TYPE_WOFF2, directwrite.dwrite_container_type, dwrite_3/DWRITE_CONTAINER_TYPE, dwrite_3/DWRITE_CONTAINER_TYPE_UNKNOWN, dwrite_3/DWRITE_CONTAINER_TYPE_WOFF, dwrite_3/DWRITE_CONTAINER_TYPE_WOFF2
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
 - DWRITE_CONTAINER_TYPE
 - dwrite_3/DWRITE_CONTAINER_TYPE
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
 - DWRITE_CONTAINER_TYPE
---

# DWRITE_CONTAINER_TYPE enumeration


## -description

Specifies the container format of a font resource. A container format is distinct from
          a font file format (DWRITE_FONT_FILE_TYPE) because the container describes the container
          in which the underlying font file is packaged.

## -enum-fields

### -field DWRITE_CONTAINER_TYPE_UNKNOWN

### -field DWRITE_CONTAINER_TYPE_WOFF

### -field DWRITE_CONTAINER_TYPE_WOFF2

## -remarks

DWRITE_CONTAINER_TYPE is returned by <a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype">IDWriteFactory5::AnalyzeContainerType</a>

