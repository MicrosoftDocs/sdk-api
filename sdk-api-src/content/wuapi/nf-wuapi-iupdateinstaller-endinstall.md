---
UID: NF:wuapi.IUpdateInstaller.EndInstall
title: IUpdateInstaller::EndInstall (wuapi.h)
author: windows-sdk-content
description: Completes an asynchronous installation of the updates.
old-location: wua\iupdateinstaller_endinstall.htm
tech.root: Wua_Sdk
ms.assetid: 7137164c-2b82-48dc-8488-6c8872896a39
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndInstall, EndInstall method [Windows Update Agent], EndInstall method [Windows Update Agent],IUpdateInstaller interface, IUpdateInstaller interface [Windows Update Agent],EndInstall method, IUpdateInstaller.EndInstall, IUpdateInstaller::EndInstall, wua.iupdateinstaller_endinstall, wuapi/IUpdateInstaller::EndInstall
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
 - IUpdateInstaller.EndInstall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateInstaller::EndInstall


## -description


Completes an asynchronous installation of the updates.


## -parameters




### -param value [in]

The <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationjob">IInstallationJob</a> interface that is  returned by the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-begininstall">BeginInstall</a> method.


### -param retval [out]

An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationresult">IInstallationResult</a> interface that represents the overall result of the installation operation.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows 

error code.




## -remarks



When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://docs.microsoft.com/windows/desktop/Wua_Sdk/guidelines-for-asynchronous-wua-operations">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a>
 

 

