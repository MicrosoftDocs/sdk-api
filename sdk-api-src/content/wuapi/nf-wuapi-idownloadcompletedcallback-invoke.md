---
UID: NF:wuapi.IDownloadCompletedCallback.Invoke
title: IDownloadCompletedCallback::Invoke
author: windows-sdk-content
description: Notifies the caller that the download is complete.
old-location: wua\idownloadcompletedcallback_invoke.htm
tech.root: Wua_Sdk
ms.assetid: 87334ff3-bfb0-48cb-b2e1-ea6d4617638d
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IDownloadCompletedCallback interface [Windows Update Agent],Invoke method, IDownloadCompletedCallback.Invoke, IDownloadCompletedCallback::Invoke, Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent],IDownloadCompletedCallback interface, wua.idownloadcompletedcallback_invoke, wuapi/IDownloadCompletedCallback::Invoke
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
 - IDownloadCompletedCallback.Invoke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDownloadCompletedCallback::Invoke


## -description


Notifies the caller that the download is complete.


## -parameters




### -param downloadJob

TBD


### -param callbackArgs [in]

This parameter is reserved for future use and can be ignored.


#### - searchJob [in]

An <a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a> interface that contains download information.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/ad1c3075-21d9-409f-9677-fbf6d0c50313">IDownloadCompletedCallback</a>



<a href="https://msdn.microsoft.com/9a953240-3d8e-4876-92a9-cc7efca62780">IUpdateDownloader::BeginDownload</a>
 

 

