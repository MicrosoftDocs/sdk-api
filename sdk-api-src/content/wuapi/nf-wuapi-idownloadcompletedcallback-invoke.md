---
UID: NF:wuapi.IDownloadCompletedCallback.Invoke
title: IDownloadCompletedCallback::Invoke (wuapi.h)
description: Notifies the caller that the download is complete.
old-location: wua\idownloadcompletedcallback_invoke.htm
tech.root: Wua_Sdk
ms.assetid: 87334ff3-bfb0-48cb-b2e1-ea6d4617638d
ms.date: 12/05/2018
ms.keywords: IDownloadCompletedCallback interface [Windows Update Agent],Invoke method, IDownloadCompletedCallback.Invoke, IDownloadCompletedCallback::Invoke, Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent],IDownloadCompletedCallback interface, wua.idownloadcompletedcallback_invoke, wuapi/IDownloadCompletedCallback::Invoke
f1_keywords:
- wuapi/IDownloadCompletedCallback.Invoke
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wuapi.dll
api_name:
- IDownloadCompletedCallback.Invoke
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDownloadCompletedCallback::Invoke


## -description


Notifies the caller that the download is complete.


## -parameters




### -param downloadJob [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-idownloadjob">IDownloadJob</a> interface that contains download information.


### -param callbackArgs [in]

This parameter is reserved for future use and can be ignored.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-idownloadcompletedcallback">IDownloadCompletedCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatedownloader-begindownload">IUpdateDownloader::BeginDownload</a>
 

 

