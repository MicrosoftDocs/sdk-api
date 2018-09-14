---
UID: NF:wuapi.IInstallationCompletedCallback.Invoke
title: IInstallationCompletedCallback::Invoke
author: windows-sdk-content
description: Handles the notification of the completion of an asynchronous installation or uninstallation that is initiated by a call to IUpdateInstaller.BeginInstall or IUpdateInstaller.BeginUninstall.
old-location: wua\iinstallationcompletedcallback_invoke.htm
tech.root: Wua_Sdk
ms.assetid: b7c413b2-b485-41a5-b2c9-5c3e9c10427c
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IInstallationCompletedCallback interface [Windows Update Agent],Invoke method, IInstallationCompletedCallback.Invoke, IInstallationCompletedCallback::Invoke, Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent],IInstallationCompletedCallback interface, wua.iinstallationcompletedcallback_invoke, wuapi/IInstallationCompletedCallback::Invoke
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
 - IInstallationCompletedCallback.Invoke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInstallationCompletedCallback::Invoke


## -description


Handles the notification of the completion of an asynchronous installation or uninstallation that is initiated by a call to <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller.BeginInstall</a> or <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">IUpdateInstaller.BeginUninstall</a>.


## -parameters




### -param installationJob [in]

An <a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a> interface that contains the installation information.


### -param callbackArgs [in]

This parameter is reserved for future use and can be ignored.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/930d33e1-e407-4306-acc6-1d64c385a41d">IInstallationCompletedCallback</a>



<a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller::BeginInstall</a>
 

 

