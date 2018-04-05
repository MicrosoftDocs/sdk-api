---
UID: NF:wuapi.IInstallationProgressChangedCallback.Invoke
title: IInstallationProgressChangedCallback::Invoke method
author: windows-driver-content
description: Handles the notification of the change in the progress of an asynchronous installation or uninstallation that was initiated by a call to the IUpdateInstaller.BeginInstall method or the IUpdateInstaller.BeginUninstall method.
old-location: wua\iinstallationprogresschangedcallback_invoke.htm
old-project: Wua_Sdk
ms.assetid: 1ef4ab68-8bf3-4141-aba2-826bb606eab5
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: IInstallationProgressChangedCallback, IInstallationProgressChangedCallback interface [Windows Update Agent], Invoke method, IInstallationProgressChangedCallback::Invoke, Invoke method [Windows Update Agent], Invoke method [Windows Update Agent], IInstallationProgressChangedCallback interface, Invoke,IInstallationProgressChangedCallback.Invoke, wua.iinstallationprogresschangedcallback_invoke, wuapi/IInstallationProgressChangedCallback::Invoke
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
-	IInstallationProgressChangedCallback.Invoke
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IInstallationProgressChangedCallback::Invoke method


## -description


Handles the notification of the change in the progress of an asynchronous installation or uninstallation that was initiated by a call to the <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller.BeginInstall</a> method or the <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">IUpdateInstaller.BeginUninstall</a> method.


## -parameters




### -param installationJob




### -param callbackArgs [in]

An <a href="https://msdn.microsoft.com/9175bcaf-8015-466d-ae0c-7ba685bdf192">IInstallationProgressChangedCallbackArgs</a> interface that contains the installation progress data.


#### - downloadJob [in]

An <a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a> interface that contains the installation information.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns  a COM or Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/a092dbba-57a4-4deb-be05-26cfa29e33aa">IInstallationProgressChangedCallback</a>



<a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">IUpdateInstaller::BeginInstall</a>
 

 

