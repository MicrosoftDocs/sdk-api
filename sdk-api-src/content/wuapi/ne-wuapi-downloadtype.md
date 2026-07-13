---
UID: NE:wuapi.tagDownloadType
tech.root: wua
title: DownloadType
ms.date: 08/13/2024
targetos: Windows
description: Specifies the type of download to perform.
prerelease: true
req.construct-type: enumeration
req.ddi-compliance: 
req.header: wuapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 Build 26100
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - wuapi.h
api_name:
 - tagDownloadType
 - DownloadType
f1_keywords:
 - tagDownloadType
 - wuapi/tagDownloadType
 - DownloadType
 - wuapi/DownloadType
dev_langs:
 - c++
helpviewer_keywords:
 - tagDownloadType
---

## -description

Specifies the type of update download to perform.

## -enum-fields

### -field downloadTypeFull

A full update download.

### -field downloadTypeUpdateBootstrapper

A download containing only the update bootstrapper.

## -remarks

The values from this enumeration are used by methods of the [IUpdateDownloaderEx](nn-wuapi-iupdatedownloaderex.md) interface to specify whether a full download should be performed or only the update bootstrapper should be downloaded. If a caller chooses to only download the update bootstrapper, they are still expected to perform a full download later before they can install the update.

## -see-also

[IUpdateDownloaderEx::BeginDownload2](nf-wuapi-iupdatedownloaderex-begindownload2.md)

[IUpdateDownloaderEx::Download2](nf-wuapi-iupdatedownloaderex-download2.md)
