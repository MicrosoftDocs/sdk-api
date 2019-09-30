---
UID: NF:wuapi.IInstallationJob.GetProgress
title: IInstallationJob::GetProgress (wuapi.h)
author: windows-sdk-content
description: Returns an IInstallationProgress interface that describes the current progress of an installation or uninstallation.
old-location: wua\iinstallationjob_getprogress.htm
tech.root: Wua_Sdk
ms.assetid: 7d63ec9d-bf7a-4c5d-a1e7-4dcc0f236d07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetProgress, GetProgress method [Windows Update Agent], GetProgress method [Windows Update Agent],IInstallationJob interface, IInstallationJob interface [Windows Update Agent],GetProgress method, IInstallationJob.GetProgress, IInstallationJob::GetProgress, wua.iinstallationjob_getprogress, wuapi/IInstallationJob::GetProgress
ms.topic: method
f1_keywords: 
 - "wuapi/IInstallationJob.GetProgress"
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
 - IInstallationJob.GetProgress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInstallationJob::GetProgress


## -description


Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationprogress">IInstallationProgress</a> interface that describes the current progress of an installation or uninstallation.


## -parameters




### -param retval [out]

An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationprogress">IInstallationProgress</a> interface that describes the current progress of an installation or uninstallation.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



You must make repeated calls to the <b>GetProgress</b> method to track the progress of a download. You must do this because  
the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateinstallationresult">IUpdateInstallationResult</a> interface is not automatically updated during a download.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationjob">IInstallationJob</a>
 

 

