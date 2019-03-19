---
UID: NF:wuapi.IInstallationProgress.GetUpdateResult
title: IInstallationProgress::GetUpdateResult (wuapi.h)
author: windows-sdk-content
description: Returns the result of the installation or uninstallation of a specified update.
old-location: wua\iinstallationprogress_getupdateresult.htm
tech.root: Wua_Sdk
ms.assetid: a0cb92f4-6c97-42be-abf1-e1662e213a7d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetUpdateResult, GetUpdateResult method [Windows Update Agent], GetUpdateResult method [Windows Update Agent],IInstallationProgress interface, IInstallationProgress interface [Windows Update Agent],GetUpdateResult method, IInstallationProgress.GetUpdateResult, IInstallationProgress::GetUpdateResult, wua.iinstallationprogress_getupdateresult, wuapi/IInstallationProgress::GetUpdateResult
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
 - IInstallationProgress.GetUpdateResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInstallationProgress::GetUpdateResult


## -description


Returns the result of the installation or uninstallation of a specified update.


## -parameters




### -param updateIndex [in]

A zero-based index value that specifies an update.


### -param retval [out]

An <a href="https://msdn.microsoft.com/6c27d691-d9b1-41ce-b3e8-dd2574c19b8b">IUpdateInstallationResult</a> interface that contains information about a specified update.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -remarks



You must make repeated calls to the <b>GetUpdateResult</b> method to track the progress of a download. You must do this because  
the <a href="https://msdn.microsoft.com/6c27d691-d9b1-41ce-b3e8-dd2574c19b8b">IUpdateInstallationResult</a> interface is not automatically updated during a download.




## -see-also




<a href="https://msdn.microsoft.com/aa7e0c4d-9cb3-4473-a3b9-02ff9643f7de">IInstallationProgress</a>
 

 

