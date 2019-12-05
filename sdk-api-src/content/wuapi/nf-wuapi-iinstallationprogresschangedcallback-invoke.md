---
UID: NF:wuapi.IInstallationProgressChangedCallback.Invoke
title: IInstallationProgressChangedCallback::Invoke (wuapi.h)
description: Handles the notification of the change in the progress of an asynchronous installation or uninstallation that was initiated by a call to the IUpdateInstaller.BeginInstall method or the IUpdateInstaller.BeginUninstall method.
old-location: wua\iinstallationprogresschangedcallback_invoke.htm
tech.root: Wua_Sdk
ms.assetid: 1ef4ab68-8bf3-4141-aba2-826bb606eab5
ms.date: 12/05/2018
ms.keywords: IInstallationProgressChangedCallback interface [Windows Update Agent],Invoke method, IInstallationProgressChangedCallback.Invoke, IInstallationProgressChangedCallback::Invoke, Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent],IInstallationProgressChangedCallback interface, wua.iinstallationprogresschangedcallback_invoke, wuapi/IInstallationProgressChangedCallback::Invoke
ms.topic: method
f1_keywords:
- wuapi/IInstallationProgressChangedCallback.Invoke
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
- IInstallationProgressChangedCallback.Invoke
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInstallationProgressChangedCallback::Invoke


## -description


Handles the notification of the change in the progress of an asynchronous installation or uninstallation that was initiated by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller.BeginInstall</a> method or the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">IUpdateInstaller.BeginUninstall</a> method.


## -parameters




### -param installationJob [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationjob">IInstallationJob</a> interface that contains the installation information.


### -param callbackArgs [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationprogresschangedcallbackargs">IInstallationProgressChangedCallbackArgs</a> interface that contains the installation progress data.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns  a COM or Windows error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationprogresschangedcallback">IInstallationProgressChangedCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller::BeginInstall</a>
 

 

