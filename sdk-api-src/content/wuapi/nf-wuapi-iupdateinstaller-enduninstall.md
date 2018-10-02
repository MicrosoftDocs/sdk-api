---
UID: NF:wuapi.IUpdateInstaller.EndUninstall
title: IUpdateInstaller::EndUninstall
author: windows-sdk-content
description: Completes an asynchronous uninstallation of the updates.
old-location: wua\iupdateinstaller_enduninstall.htm
tech.root: Wua_Sdk
ms.assetid: a035f566-7ec6-41d5-b5b4-69c2acaa8aae
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: EndUninstall, EndUninstall method [Windows Update Agent], EndUninstall method [Windows Update Agent],IUpdateInstaller interface, IUpdateInstaller interface [Windows Update Agent],EndUninstall method, IUpdateInstaller.EndUninstall, IUpdateInstaller::EndUninstall, wua.iupdateinstaller_enduninstall, wuapi/IUpdateInstaller::EndUninstall
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
 - IUpdateInstaller.EndUninstall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateInstaller::EndUninstall


## -description


Completes an asynchronous uninstallation of the updates.


## -parameters




### -param value [in]

The <a href="https://msdn.microsoft.com/1a83a44e-cd3b-43b0-8741-a73fe9954063">IInstallationJob</a> interface  that the <a href="https://msdn.microsoft.com/6ff82120-aa8f-4daf-b9f9-e0129fad0a24">BeginUninstall</a> method returns.


### -param retval [out]

An <a href="https://msdn.microsoft.com/453945d7-11a3-4237-b1c8-928194be558d">IInstallationResult</a> interface that represents the overall result of an uninstallation operation.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows 

error code.




## -remarks



When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a>
 

 

