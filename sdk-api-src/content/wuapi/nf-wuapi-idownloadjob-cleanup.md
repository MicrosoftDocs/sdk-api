---
UID: NF:wuapi.IDownloadJob.CleanUp
title: IDownloadJob::CleanUp method
author: windows-driver-content
description: Waits for an asynchronous operation to be completed and releases all callbacks.
old-location: wua\idownloadjob_cleanup.htm
old-project: Wua_Sdk
ms.assetid: 0910acbc-81d7-44ae-bae1-26c82b33d29b
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CleanUp method [Windows Update Agent], CleanUp method [Windows Update Agent], IDownloadJob interface, CleanUp,IDownloadJob.CleanUp, IDownloadJob, IDownloadJob interface [Windows Update Agent], CleanUp method, IDownloadJob::CleanUp, wua.idownloadjob_cleanup, wuapi/IDownloadJob::CleanUp
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
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IDownloadJob.CleanUp
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IDownloadJob::CleanUp method


## -description


Waits for an asynchronous operation to be completed and releases all callbacks.


## -parameters






## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/0157acab-53b6-43f9-a358-81cd5108c531">IDownloadJob</a>
 

 

