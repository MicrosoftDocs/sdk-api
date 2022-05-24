---
UID: NS:deliveryoptimization._DO_DOWNLOAD_RANGES_INFO
tech.root: delivery_optimization
title: DO_DOWNLOAD_RANGES_INFO
ms.date: 05/04/2022
targetos: Windows
description: Identifies an array of ranges of bytes to download from a file.
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
req.typenames: DO_DOWNLOAD_RANGES_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - deliveryoptimization.h
api_name:
 - _DO_DOWNLOAD_RANGES_INFO
 - DO_DOWNLOAD_RANGES_INFO
f1_keywords:
 - _DO_DOWNLOAD_RANGES_INFO
 - deliveryoptimization/_DO_DOWNLOAD_RANGES_INFO
 - DO_DOWNLOAD_RANGES_INFO
 - deliveryoptimization/DO_DOWNLOAD_RANGES_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - _DO_DOWNLOAD_RANGES_INFO
prerelease: false
---

## -description

The **DO_DOWNLOAD_RANGES_INFO** structure identifies an array of ranges of bytes to download from a file. It is typically passed as an optional argument to the **IDODownload::Start** function.

## -struct-fields

### -field RangeCount

Number of elements in Ranges.

### -field Ranges

Array of one or more **DO_DOWNLOAD_RANGE** structures that specify the ranges to download.

## -remarks

## -see-also
