---
UID: NS:compressapi._COMPRESS_ALLOCATION_ROUTINES
title: COMPRESS_ALLOCATION_ROUTINES (compressapi.h)
description: A structure containing optional memory allocation and deallocation routines.
helpviewer_keywords: ["*PCOMPRESS_ALLOCATION_ROUTINES","COMPRESS_ALLOCATION_ROUTINES","COMPRESS_ALLOCATION_ROUTINES structure [Compression API]","PCOMPRESS_ALLOCATION_ROUTINES","PCOMPRESS_ALLOCATION_ROUTINES structure pointer [Compression API]","cmpapi.compress_allocation_routines","compressapi/COMPRESS_ALLOCATION_ROUTINES","compressapi/PCOMPRESS_ALLOCATION_ROUTINES"]
old-location: cmpapi\compress_allocation_routines.htm
tech.root: cmpapi
ms.assetid: 91f541c8-36b9-4ec2-ae37-0b41aa6fd623
ms.date: 12/05/2018
ms.keywords: '*PCOMPRESS_ALLOCATION_ROUTINES, COMPRESS_ALLOCATION_ROUTINES, COMPRESS_ALLOCATION_ROUTINES structure [Compression API], PCOMPRESS_ALLOCATION_ROUTINES, PCOMPRESS_ALLOCATION_ROUTINES structure pointer [Compression API], cmpapi.compress_allocation_routines, compressapi/COMPRESS_ALLOCATION_ROUTINES, compressapi/PCOMPRESS_ALLOCATION_ROUTINES'
req.header: compressapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: COMPRESS_ALLOCATION_ROUTINES, *PCOMPRESS_ALLOCATION_ROUTINES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _COMPRESS_ALLOCATION_ROUTINES
 - compressapi/_COMPRESS_ALLOCATION_ROUTINES
 - PCOMPRESS_ALLOCATION_ROUTINES
 - compressapi/PCOMPRESS_ALLOCATION_ROUTINES
 - COMPRESS_ALLOCATION_ROUTINES
 - compressapi/COMPRESS_ALLOCATION_ROUTINES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - compressapi.h
api_name:
 - COMPRESS_ALLOCATION_ROUTINES
---

# COMPRESS_ALLOCATION_ROUTINES structure


## -description

A structure containing optional memory allocation and deallocation routines.

## -struct-fields

### -field Allocate

Callback that allocates memory.

### -field Free

Callback that deallocates memory.

### -field UserContext

A pointer to context information for the allocation or deallocation routine defined by the user.

