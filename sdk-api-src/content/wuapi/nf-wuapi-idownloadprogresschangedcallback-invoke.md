---
UID: NF:wuapi.IDownloadProgressChangedCallback.Invoke
title: IDownloadProgressChangedCallback::Invoke
author: windows-sdk-content
description: Handles the notification of a change in the progress of an asynchronous download that was initiated by calling the IUpdateDownloader.BeginDownload method.
old-location: wua\idownloadprogresschangedcallback_invoke.htm
tech.root: wua_sdk
ms.assetid: 09bdbb3a-0556-4b3a-ba18-2fe7bcb33999
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IDownloadProgressChangedCallback interface [Windows Update Agent],Invoke method, IDownloadProgressChangedCallback.Invoke, IDownloadProgressChangedCallback::Invoke, Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent],IDownloadProgressChangedCallback interface, wua.idownloadprogresschangedcallback_invoke, wuapi/IDownloadProgressChangedCallback::Invoke
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
 - IDownloadProgressChangedCallback.Invoke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDownloadProgressChangedCallback::Invoke


## -description


Handles the notification of a change in the progress of an asynchronous download that was initiated by calling the <a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">IUpdateDownloader.BeginDownload</a> method.


## -parameters




### -param downloadJob [in]

An <a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a> interface that contains download information.


### -param callbackArgs [in]

An <a href="https://msdn.microsoft.com/014bb208-1241-4022-b37a-cd16da48174c">IDownloadProgressChangedCallbackArgs</a> interface that contains download progress data.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns   a COM or Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/8fc414da-835c-438f-b607-8a273e7f9064">IDownloadProgressChangedCallback</a>



<a href="https://msdn.microsoft.com/09bdbb3a-0556-4b3a-ba18-2fe7bcb33999">IUpdateDownloader::BeginDownload</a>
 

 

