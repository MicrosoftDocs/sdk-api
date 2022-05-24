---
UID: NS:deliveryoptimization._DO_DOWNLOAD_STATUS
tech.root: delivery_optimization
title: DO_DOWNLOAD_STATUS
ms.date: 05/04/2022
targetos: Windows
description: Used to obtain the status of a specific download.
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
req.typenames: DO_DOWNLOAD_STATUS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - deliveryoptimization.h
api_name:
 - _DO_DOWNLOAD_STATUS
 - DO_DOWNLOAD_STATUS
f1_keywords:
 - _DO_DOWNLOAD_STATUS
 - deliveryoptimization/_DO_DOWNLOAD_STATUS
 - DO_DOWNLOAD_STATUS
 - deliveryoptimization/DO_DOWNLOAD_STATUS
dev_langs:
 - c++
helpviewer_keywords:
 - _DO_DOWNLOAD_STATUS
prerelease: false
---

## -description

The **DO_DOWNLOAD_STATUS** structure is used to obtain the status of a specific download. It is obtained by calling the **IDODownload::GetStatus** function.

## -struct-fields

### -field BytesTotal

The total number of bytes to download.

### -field BytesTransferred

The number of bytes that have already been downloaded.

### -field State

The current download state as defined by the **DODownloadState** enumeration.

### -field Error

The error information (if it exists) that is associated with the current download.

### -field ExtendedError

The extended error information (if it exists) that is associated with the current download.

## -remarks

## -see-also
