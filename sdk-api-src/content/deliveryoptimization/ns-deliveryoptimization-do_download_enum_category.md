---
UID: NS:deliveryoptimization._DO_DOWNLOAD_ENUM_CATEGORY
tech.root: delivery_optimization
title: DO_DOWNLOAD_ENUM_CATEGORY
ms.date: 05/04/2022
targetos: Windows
description: Used by **IDOManager::EnumDownloads** to filter the downloads enumeration by the specific property's value.
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
req.typenames: DO_DOWNLOAD_ENUM_CATEGORY
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - deliveryoptimization.h
api_name:
 - _DO_DOWNLOAD_ENUM_CATEGORY
 - DO_DOWNLOAD_ENUM_CATEGORY
f1_keywords:
 - _DO_DOWNLOAD_ENUM_CATEGORY
 - deliveryoptimization/_DO_DOWNLOAD_ENUM_CATEGORY
 - DO_DOWNLOAD_ENUM_CATEGORY
 - deliveryoptimization/DO_DOWNLOAD_ENUM_CATEGORY
dev_langs:
 - c++
helpviewer_keywords:
 - _DO_DOWNLOAD_ENUM_CATEGORY
prerelease: false
---

## -description

The **DO_DOWNLOAD_ENUM_CATEGORY** structure is used by **IDOManager::EnumDownloads** to filter the downloads enumeration by the specific property's value.

## -struct-fields

### -field Property

The property name to be used for the download enumeration. These properties are supported for enumeration purposes.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

### -field Value

The property's value.

## -remarks

## -see-also
