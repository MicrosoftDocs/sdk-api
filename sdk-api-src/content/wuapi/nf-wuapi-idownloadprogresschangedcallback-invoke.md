---
UID: NF:wuapi.IDownloadProgressChangedCallback.Invoke
title: IDownloadProgressChangedCallback::Invoke (wuapi.h)
description: Handles the notification of a change in the progress of an asynchronous download that was initiated by calling the IUpdateDownloader.BeginDownload method.
helpviewer_keywords: ["IDownloadProgressChangedCallback interface [Windows Update Agent]","Invoke method","IDownloadProgressChangedCallback.Invoke","IDownloadProgressChangedCallback::Invoke","Invoke","Invoke method [Windows Update Agent]","Invoke method [Windows Update Agent]","IDownloadProgressChangedCallback interface","wua.idownloadprogresschangedcallback_invoke","wuapi/IDownloadProgressChangedCallback::Invoke"]
old-location: wua\idownloadprogresschangedcallback_invoke.htm
tech.root: wua
ms.assetid: 09bdbb3a-0556-4b3a-ba18-2fe7bcb33999
ms.date: 12/05/2018
ms.keywords: IDownloadProgressChangedCallback interface [Windows Update Agent],Invoke method, IDownloadProgressChangedCallback.Invoke, IDownloadProgressChangedCallback::Invoke, Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent],IDownloadProgressChangedCallback interface, wua.idownloadprogresschangedcallback_invoke, wuapi/IDownloadProgressChangedCallback::Invoke
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDownloadProgressChangedCallback::Invoke
 - wuapi/IDownloadProgressChangedCallback::Invoke
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IDownloadProgressChangedCallback.Invoke
---

# IDownloadProgressChangedCallback::Invoke


## -description

Handles the notification of a change in the progress of an asynchronous download that was initiated by calling the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader.BeginDownload</a> method.

## -parameters

### -param downloadJob [in]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadjob">IDownloadJob</a> interface that contains download information.

### -param callbackArgs [in]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadprogresschangedcallbackargs">IDownloadProgressChangedCallbackArgs</a> interface that contains download progress data.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns   a COM or Windows error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadprogresschangedcallback">IDownloadProgressChangedCallback</a>



<a href="/windows/desktop/api/wuapi/nf-wuapi-idownloadprogresschangedcallback-invoke">IUpdateDownloader::BeginDownload</a>