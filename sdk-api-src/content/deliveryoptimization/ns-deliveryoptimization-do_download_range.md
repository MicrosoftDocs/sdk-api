---
UID: NS:deliveryoptimization._DO_DOWNLOAD_RANGE
tech.root: delivery_optimization
title: DO_DOWNLOAD_RANGE
ms.date: 05/04/2022
targetos: Windows
description: Identifies a single range of bytes to download from a file.
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: deliveryoptimization.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.target-type: 
req.typenames: DO_DOWNLOAD_RANGE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - deliveryoptimization.h
api_name:
 - _DO_DOWNLOAD_RANGE
 - DO_DOWNLOAD_RANGE
f1_keywords:
 - _DO_DOWNLOAD_RANGE
 - deliveryoptimization/_DO_DOWNLOAD_RANGE
 - DO_DOWNLOAD_RANGE
 - deliveryoptimization/DO_DOWNLOAD_RANGE
dev_langs:
 - c++
helpviewer_keywords:
 - _DO_DOWNLOAD_RANGE
prerelease: false
---

## -description

The **DO_DOWNLOAD_RANGE** structure identifies a single range of bytes to download from a file. The **DO_DOWNLOAD_RANGE** structure is included within **DO_DOWNLOAD_RANGES_INFO** structure to provide an array of ranges to download.

## -struct-fields

### -field Offset

Zero-based offset to the beginning of the range of bytes to download from a file.

### -field Length

The length of the range, in bytes. Do not specify a zero-byte length. To indicate that the range extends to the end of the file, specify **DO_LENGTH_TO_EOF**.

## -remarks

## -see-also
