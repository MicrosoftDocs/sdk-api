---
UID: NF:wuapi.IUpdateInstaller.EndInstall
title: IUpdateInstaller::EndInstall
author: windows-sdk-content
description: Completes an asynchronous installation of the updates.
old-location: wua\iupdateinstaller_endinstall.htm
old-project: Wua_Sdk
ms.assetid: 7137164c-2b82-48dc-8488-6c8872896a39
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: EndInstall, EndInstall method [Windows Update Agent], EndInstall method [Windows Update Agent],IUpdateInstaller interface, IUpdateInstaller interface [Windows Update Agent],EndInstall method, IUpdateInstaller.EndInstall, IUpdateInstaller::EndInstall, wua.iupdateinstaller_endinstall, wuapi/IUpdateInstaller::EndInstall
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
 - IUpdateInstaller.EndInstall
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateInstaller::EndInstall


## -description


Completes an asynchronous installation of the updates.


## -parameters




### -param value [in]

The <a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a> interface that is  returned by the <a href="https://msdn.microsoft.com/756ad613-bc6b-48fb-a079-c192aa98ccfe">BeginInstall</a> method.


### -param retval [out]

An <a href="https://msdn.microsoft.com/453945d7-11a3-4237-b1c8-928194be558d">IInstallationResult</a> interface that represents the overall result of the installation operation.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows 

error code.




## -remarks



When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a>
 

 

