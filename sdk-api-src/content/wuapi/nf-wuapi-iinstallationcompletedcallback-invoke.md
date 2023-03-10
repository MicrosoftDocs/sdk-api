---
UID: NF:wuapi.IInstallationCompletedCallback.Invoke
title: IInstallationCompletedCallback::Invoke (wuapi.h)
description: Handles the notification of the completion of an asynchronous installation or uninstallation that is initiated by a call to IUpdateInstaller.BeginInstall or IUpdateInstaller.BeginUninstall.
helpviewer_keywords: ["IInstallationCompletedCallback interface [Windows Update Agent]","Invoke method","IInstallationCompletedCallback.Invoke","IInstallationCompletedCallback::Invoke","Invoke","Invoke method [Windows Update Agent]","Invoke method [Windows Update Agent]","IInstallationCompletedCallback interface","wua.iinstallationcompletedcallback_invoke","wuapi/IInstallationCompletedCallback::Invoke"]
old-location: wua\iinstallationcompletedcallback_invoke.htm
tech.root: wua
ms.assetid: b7c413b2-b485-41a5-b2c9-5c3e9c10427c
ms.date: 12/05/2018
ms.keywords: IInstallationCompletedCallback interface [Windows Update Agent],Invoke method, IInstallationCompletedCallback.Invoke, IInstallationCompletedCallback::Invoke, Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent],IInstallationCompletedCallback interface, wua.iinstallationcompletedcallback_invoke, wuapi/IInstallationCompletedCallback::Invoke
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
 - IInstallationCompletedCallback::Invoke
 - wuapi/IInstallationCompletedCallback::Invoke
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
 - IInstallationCompletedCallback.Invoke
---

# IInstallationCompletedCallback::Invoke


## -description

Handles the notification of the completion of an asynchronous installation or uninstallation that is initiated by a call to <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller.BeginInstall</a> or <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">IUpdateInstaller.BeginUninstall</a>.

## -parameters

### -param installationJob [in]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationjob">IInstallationJob</a> interface that contains the installation information.

### -param callbackArgs [in]

This parameter is reserved for future use and can be ignored.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationcompletedcallback">IInstallationCompletedCallback</a>



<a href="/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">IUpdateInstaller::BeginInstall</a>