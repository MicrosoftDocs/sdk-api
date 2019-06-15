---
UID: NF:wuapi.IUpdateInstaller.EndUninstall
title: IUpdateInstaller::EndUninstall (wuapi.h)
author: windows-sdk-content
description: Completes an asynchronous uninstallation of the updates.
old-location: wua\iupdateinstaller_enduninstall.htm
tech.root: Wua_Sdk
ms.assetid: a035f566-7ec6-41d5-b5b4-69c2acaa8aae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EndUninstall, EndUninstall method [Windows Update Agent], EndUninstall method [Windows Update Agent],IUpdateInstaller interface, IUpdateInstaller interface [Windows Update Agent],EndUninstall method, IUpdateInstaller.EndUninstall, IUpdateInstaller::EndUninstall, wua.iupdateinstaller_enduninstall, wuapi/IUpdateInstaller::EndUninstall
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
ms.custom: 19H1
---

# IUpdateInstaller::EndUninstall


## -description


Completes an asynchronous uninstallation of the updates.


## -parameters




### -param value [in]

The <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationjob">IInstallationJob</a> interface  that the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdateinstaller-beginuninstall">BeginUninstall</a> method returns.


### -param retval [out]

An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iinstallationresult">IInstallationResult</a> interface that represents the overall result of an uninstallation operation.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows 

error code.




## -remarks



When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://docs.microsoft.com/windows/desktop/Wua_Sdk/guidelines-for-asynchronous-wua-operations">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a>
 

 

