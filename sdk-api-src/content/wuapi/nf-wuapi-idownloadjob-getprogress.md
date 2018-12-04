---
UID: NF:wuapi.IDownloadJob.GetProgress
title: IDownloadJob::GetProgress
author: windows-sdk-content
description: Returns an IDownloadProgress interface that describes the current progress of a download.
old-location: wua\idownloadjob_getprogress.htm
tech.root: wua_sdk
ms.assetid: e87c85cf-0011-4edb-a409-0b4db3292caf
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetProgress, GetProgress method [Windows Update Agent], GetProgress method [Windows Update Agent],IDownloadJob interface, IDownloadJob interface [Windows Update Agent],GetProgress method, IDownloadJob.GetProgress, IDownloadJob::GetProgress, wua.idownloadjob_getprogress, wuapi/IDownloadJob::GetProgress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDownloadJob::GetProgress


## -description


Returns an <a href="https://msdn.microsoft.com/773de760-5fde-4975-ba8d-d20b3affb4a7">IDownloadProgress</a> interface that describes the current progress of a download.


## -parameters




### -param retval [out]

An <a href="https://msdn.microsoft.com/773de760-5fde-4975-ba8d-d20b3affb4a7">IDownloadProgress</a> interface that describes the current progress of a download.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



You must make repeated calls to <b>GetProgress</b> to track the progress of a download. You must do this because  
the <a href="https://msdn.microsoft.com/773de760-5fde-4975-ba8d-d20b3affb4a7">IDownloadProgress</a> interface is not automatically updated during a download.




## -see-also




<a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a>
 

 

