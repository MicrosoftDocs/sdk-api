---
UID: NF:wuapi.IUpdateInstaller.get_IsForced
title: IUpdateInstaller::get_IsForced
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates whether to forcibly install or uninstall an update.
old-location: wua\iupdateinstaller_isforced.htm
old-project: Wua_Sdk
ms.assetid: 80a30a21-9369-44bb-984a-2fdf2c1810e4
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IUpdateInstaller interface [Windows Update Agent],IsForced property, IUpdateInstaller.IsForced, IUpdateInstaller.get_IsForced, IUpdateInstaller::IsForced, IUpdateInstaller::get_IsForced, IUpdateInstaller::put_IsForced, IsForced property [Windows Update Agent], IsForced property [Windows Update Agent],IUpdateInstaller interface, get_IsForced, wua.iupdateinstaller_isforced, wuapi/IUpdateInstaller::IsForced, wuapi/IUpdateInstaller::get_IsForced, wuapi/IUpdateInstaller::put_IsForced
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
 - IUpdateInstaller.IsForced
 - IUpdateInstaller.get_IsForced
 - IUpdateInstaller.put_IsForced
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateInstaller::get_IsForced


## -description


Gets or sets a Boolean value that indicates whether  to  forcibly install or uninstall an update.

This property is read/write.


## -parameters


## -remarks



A forced installation is an installation in which an update is installed even if the metadata indicates that the update is already installed.  A forced uninstallation is an uninstallation in which an update is removed even if the metadata indicates that the update is not installed.

Before you use <b>IsForced</b> to force an installation, determine whether the update is installed and available. If an update is not  installed, a forced installation fails. For example, an update can be downloaded, and then its corresponding files removed from the cache after the expiration limit.   In this case, if the files are not installed, a forced installation of the update  fails.




## -see-also




<a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a>
 

 

