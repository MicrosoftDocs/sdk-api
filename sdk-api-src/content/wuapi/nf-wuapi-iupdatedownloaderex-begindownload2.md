---
UID: NF:wuapi.IUpdateDownloaderEx.BeginDownload2
tech.root: wua
title: IUpdateDownloaderEx::BeginDownload2
ms.date: 08/13/2024
targetos: Windows
description: Starts an asynchronous download of the content files that are associated with the updates. (IUpdateDownloaderEx)
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
 - IUpdateDownloaderEx::BeginDownload2
f1_keywords:
 - IUpdateDownloaderEx::BeginDownload2
 - wuapi/IUpdateDownloaderEx::BeginDownload2
dev_langs:
 - c++
helpviewer_keywords:
 - BeginDownload2
---

## -description

Starts an asynchronous download of the content files that are associated with the updates. 

## -parameters

### -param downloadType

A value from the [DownloadType](ne-wuapi-downloadtype.md) specifying the type of download to perform, full download or downloading only the update bootstrapper.

> [!NOTE]
> Attempting to download the update bootstrapper for an update that does not contain one will fail with the error code WU_E_NOT_SUPPORTED.

### -param onProgressChanged

An [IDownloadProgressChangedCallback](nn-wuapi-idownloadprogresschangedcallback.md) interface that is called periodically for download progress changes before download is complete.

### -param onCompleted

An [IDownloadCompletedCallback](nn-wuapi-idownloadcompletedcallback.md) interface that is called when an asynchronous download operation is complete.

### -param state

The caller-specific state that the [AsyncState](nf-wuapi-idownloadjob-get_asyncstate.md) property of the [IDownloadJob](nn-wuapi-idownloadjob.md) interface returns. A caller may use this parameter to attach a value to the download job object. This  allows the caller to retrieve custom information about that download job object at a later time.

> [!NOTE]
>  The **AsyncState** property of the **IDownloadJob** interface can be retrieved, but it cannot be set. This does not prevent the caller from changing the contents of the object already set to the **AsyncState** property of the **IDownloadJob** interface. In other words, if the **AsyncState** property contains a number, the number cannot be changed. But, if the **AsyncState** property contains a safe array or an object, the contents of the safe array or the object can be changed at will. The value is released when the caller releases **IDownloadJob** by calling [IUpdateDownloader::EndDownload](nf-wuapi-iupdatedownloader-enddownload.md).

### -param retval

An [IDownloadJob](/windows/desktop/api/wuapi/nn-wuapi-idownloadjob) interface that contains the properties and methods that are available to a download operation that has started.

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

As an alternative to implementing the [IDownloadProgressChangedCallback](n-wuapi-idownloadprogresschangedcallback.md) interface, you can use a script to implement a callback routine of any identifier with DISPID 0 on an automation object. The type of the  *onProgressChanged* parameter is **IUnknown**.

As an alternative to implementing the [IDownloadCompletedCallback](nn-wuapi-idownloadcompletedcallback.md) interface, you can use a script to   implement a callback routine of any identifier with DISPID 0 on an automation object. The type of the *onCompleted* parameter is **IUnknown**.

This method returns **WU_E_INVALID_OPERATION** if the object that is implementing the interface is  locked down.

This method returns **WU_E_NO_UPDATE** if the [Updates](nf-wuapi-iupdatedownloader-get_updates.md) property of the [IUpdateDownloader](nn-wuapi-iupdatedownloader.md) interface is not set. This method also returns **WU_E_NO_UPDATE** if the **Updates** property is set to an empty collection.

This method returns **SUS_E_NOT_INITIALIZED** if the download job contains no updates.

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see [Guidelines for Asynchronous WUA Operations](/windows/desktop/Wua_Sdk/guidelines-for-asynchronous-wua-operations).

## -see-also

