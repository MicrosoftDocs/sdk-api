---
UID: NF:wuapi.ISearchJob.CleanUp
title: ISearchJob::CleanUp method
author: windows-driver-content
description: Waits for an asynchronous operation to complete and then releases all the callbacks.
old-location: wua\isearchjob_cleanup.htm
old-project: Wua_Sdk
ms.assetid: 35f345ac-cf5b-4ba6-9422-5d9da449bcdd
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CleanUp method [Windows Update Agent], CleanUp method [Windows Update Agent], ISearchJob interface, CleanUp,ISearchJob.CleanUp, ISearchJob, ISearchJob interface [Windows Update Agent], CleanUp method, ISearchJob::CleanUp, wua.isearchjob_cleanup, wuapi/ISearchJob::CleanUp
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
-	ISearchJob.CleanUp
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISearchJob::CleanUp method


## -description


Waits for an asynchronous operation to complete and then releases all the callbacks.


## -parameters






## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/aec4a812-cf5d-4986-a776-29c366bb1771">ISearchJob</a>
 

 

