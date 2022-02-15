---
UID: NF:wuapi.IInstallationJob.CleanUp
title: IInstallationJob::CleanUp (wuapi.h)
description: Waits for an asynchronous operation to be completed and then releases all the callbacks.
helpviewer_keywords: ["CleanUp","CleanUp method [Windows Update Agent]","CleanUp method [Windows Update Agent]","IInstallationJob interface","IInstallationJob interface [Windows Update Agent]","CleanUp method","IInstallationJob.CleanUp","IInstallationJob::CleanUp","wua.iinstallationjob_cleanup","wuapi/IInstallationJob::CleanUp"]
old-location: wua\iinstallationjob_cleanup.htm
tech.root: wua
ms.assetid: ceb42a41-9df0-4075-afbe-f8753d4543d8
ms.date: 12/05/2018
ms.keywords: CleanUp, CleanUp method [Windows Update Agent], CleanUp method [Windows Update Agent],IInstallationJob interface, IInstallationJob interface [Windows Update Agent],CleanUp method, IInstallationJob.CleanUp, IInstallationJob::CleanUp, wua.iinstallationjob_cleanup, wuapi/IInstallationJob::CleanUp
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
 - IInstallationJob::CleanUp
 - wuapi/IInstallationJob::CleanUp
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
 - IInstallationJob.CleanUp
---

# IInstallationJob::CleanUp


## -description

Waits for an asynchronous operation to be completed and then releases all the callbacks.



## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -remarks

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="/windows/desktop/Wua_Sdk/guidelines-for-asynchronous-wua-operations">Guidelines for Asynchronous WUA Operations</a>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationjob">IInstallationJob</a>
