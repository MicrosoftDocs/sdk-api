---
UID: NF:wuapi.IDownloadJob.GetProgress
title: IDownloadJob::GetProgress (wuapi.h)

description: Returns an IDownloadProgress interface that describes the current progress of a download.
old-location: wua\idownloadjob_getprogress.htm
tech.root: Wua_Sdk
ms.assetid: e87c85cf-0011-4edb-a409-0b4db3292caf

ms.date: 12/05/2018
ms.keywords: GetProgress, GetProgress method [Windows Update Agent], GetProgress method [Windows Update Agent],IDownloadJob interface, IDownloadJob interface [Windows Update Agent],GetProgress method, IDownloadJob.GetProgress, IDownloadJob::GetProgress, wua.idownloadjob_getprogress, wuapi/IDownloadJob::GetProgress
ms.topic: method
f1_keywords: 
 - "wuapi/IDownloadJob.GetProgress"
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
 - IDownloadJob.GetProgress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDownloadJob::GetProgress


## -description


Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-idownloadprogress">IDownloadProgress</a> interface that describes the current progress of a download.


## -parameters




### -param retval [out]

An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-idownloadprogress">IDownloadProgress</a> interface that describes the current progress of a download.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



You must make repeated calls to <b>GetProgress</b> to track the progress of a download. You must do this because  
the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-idownloadprogress">IDownloadProgress</a> interface is not automatically updated during a download.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-idownloadjob">IDownloadJob</a>
 

 

