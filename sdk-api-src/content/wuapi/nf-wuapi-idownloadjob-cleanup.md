---
UID: NF:wuapi.IDownloadJob.CleanUp
title: IDownloadJob::CleanUp (wuapi.h)
description: Waits for an asynchronous operation to be completed and releases all callbacks.
helpviewer_keywords: ["CleanUp","CleanUp method [Windows Update Agent]","CleanUp method [Windows Update Agent]","IDownloadJob interface","IDownloadJob interface [Windows Update Agent]","CleanUp method","IDownloadJob.CleanUp","IDownloadJob::CleanUp","wua.idownloadjob_cleanup","wuapi/IDownloadJob::CleanUp"]
old-location: wua\idownloadjob_cleanup.htm
tech.root: wua
ms.assetid: 0910acbc-81d7-44ae-bae1-26c82b33d29b
ms.date: 12/05/2018
ms.keywords: CleanUp, CleanUp method [Windows Update Agent], CleanUp method [Windows Update Agent],IDownloadJob interface, IDownloadJob interface [Windows Update Agent],CleanUp method, IDownloadJob.CleanUp, IDownloadJob::CleanUp, wua.idownloadjob_cleanup, wuapi/IDownloadJob::CleanUp
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
 - IDownloadJob::CleanUp
 - wuapi/IDownloadJob::CleanUp
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
 - IDownloadJob.CleanUp
---

# IDownloadJob::CleanUp


## -description

Waits for an asynchronous operation to be completed and releases all callbacks.



## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -remarks

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="/windows/desktop/Wua_Sdk/guidelines-for-asynchronous-wua-operations">Guidelines for Asynchronous WUA Operations</a>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-idownloadjob">IDownloadJob</a>
