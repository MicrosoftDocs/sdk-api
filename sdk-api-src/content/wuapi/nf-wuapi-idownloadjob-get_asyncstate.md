---
UID: NF:wuapi.IDownloadJob.get_AsyncState
title: IDownloadJob::get_AsyncState (wuapi.h)
description: Gets the caller-specific state object that is passed to the IUpdateDownloader.BeginDownload method.
helpviewer_keywords: ["AsyncState property [Windows Update Agent]","AsyncState property [Windows Update Agent]","IDownloadJob interface","IDownloadJob interface [Windows Update Agent]","AsyncState property","IDownloadJob.AsyncState","IDownloadJob.get_AsyncState","IDownloadJob::AsyncState","IDownloadJob::get_AsyncState","get_AsyncState","wua.idownloadjob_asyncstate","wuapi/IDownloadJob::AsyncState","wuapi/IDownloadJob::get_AsyncState"]
old-location: wua\idownloadjob_asyncstate.htm
tech.root: wua
ms.assetid: 47d2af4a-c04f-4413-ad29-3b8cb1292539
ms.date: 12/05/2018
ms.keywords: AsyncState property [Windows Update Agent], AsyncState property [Windows Update Agent],IDownloadJob interface, IDownloadJob interface [Windows Update Agent],AsyncState property, IDownloadJob.AsyncState, IDownloadJob.get_AsyncState, IDownloadJob::AsyncState, IDownloadJob::get_AsyncState, get_AsyncState, wua.idownloadjob_asyncstate, wuapi/IDownloadJob::AsyncState, wuapi/IDownloadJob::get_AsyncState
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
 - IDownloadJob::get_AsyncState
 - wuapi/IDownloadJob::get_AsyncState
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
 - IDownloadJob.AsyncState
 - IDownloadJob.get_AsyncState
---

# IDownloadJob::get_AsyncState


## -description

Gets  the caller-specific state object that is passed to the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader.BeginDownload</a> method.

This property is read-only.

## -parameters

## -remarks

This state object can be used by the caller to identify a particular download. Or, this state object can be used by the caller to pass information from the caller to the implementation of the <a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadprogresschangedcallback">IDownloadProgressChangedCallback</a>  or <a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadcompletedcallback">IDownloadCompletedCallback</a> interface.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadjob">IDownloadJob</a>