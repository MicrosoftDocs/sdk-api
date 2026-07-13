---
UID: NF:wuapi.IUpdateDownloaderEx.Download2
tech.root: wua
title: IUpdateDownloaderEx::Download2
ms.date: 08/13/2024
targetos: Windows
description: Starts a synchronous download of the content files that are associated with the updates. (IUpdateDownloaderEx)
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wuapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wuapi.h
api_name:
 - IUpdateDownloaderEx::Download2
f1_keywords:
 - IUpdateDownloaderEx::Download2
 - wuapi/IUpdateDownloaderEx::Download2
dev_langs:
 - c++
helpviewer_keywords:
 - Download2
---

## -description

Starts a synchronous download of the content files that are associated with the updates.

## -parameters

### -param downloadType

A value from the [DownloadType](ne-wuapi-downloadtype.md) specifying the type of download to perform, full download or downloading only the update bootstrapper.

> [!NOTE]
> Attempting to download the update bootstrapper for an update that does not contain one will fail with the error code WU_E_NOT_SUPPORTED.

### -param retval

An [IDownloadResult](nn-wuapi-idownloadresult.md) interface that contains result codes for the download.

## -returns

An **HRESULT** including one of the following values:

| Value | Description |
|-------|-------------|
| S_OK | Success. |
| WU_E_INVALID_OPERATION | The computer cannot access the update site. |
| WU_E_NO_UPDATE | The Windows Update Agent (WUA) does not have  updates in the collection. |
| WU_E_NOT_INITIALIZED | The Windows Update Agent (WUA) is not initialized. |
| WU_E_NOT_SUPPORTED | The update bootstrapper download was attempted on an update that doesn't contain one. |

## -remarks

This method returns **WU_E_INVALID_OPERATION** if the object that is implementing the interface is locked down.

This method returns **WU_E_NO_UPDATE** if the [Updates](nf-wuapi-iupdatedownloader-get_updates.md) property of the [IUpdateDownloader](nn-wuapi-iupdatedownloader.md) interface is not set. This method also returns **WU_E_NO_UPDATE** if the **Updates** property is set to an empty collection.

This method returns **SUS_E_NOT_INITIALIZED** if the download job does not contain updates.

## -see-also

