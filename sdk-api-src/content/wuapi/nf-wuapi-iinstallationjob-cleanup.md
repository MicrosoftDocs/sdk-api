---
UID: NF:wuapi.IInstallationJob.CleanUp
title: IInstallationJob::CleanUp
author: windows-sdk-content
description: Waits for an asynchronous operation to be completed and then releases all the callbacks.
old-location: wua\iinstallationjob_cleanup.htm
old-project: Wua_Sdk
ms.assetid: ceb42a41-9df0-4075-afbe-f8753d4543d8
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CleanUp, CleanUp method [Windows Update Agent], CleanUp method [Windows Update Agent],IInstallationJob interface, IInstallationJob interface [Windows Update Agent],CleanUp method, IInstallationJob.CleanUp, IInstallationJob::CleanUp, wua.iinstallationjob_cleanup, wuapi/IInstallationJob::CleanUp
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IInstallationJob.CleanUp
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IInstallationJob::CleanUp


## -description


Waits for an asynchronous operation to be completed and then releases all the callbacks.


## -parameters






## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a>
 

 

