---
UID: NF:fsrmscreen.IFsrmFileScreenManager.GetFileScreen
title: IFsrmFileScreenManager::GetFileScreen
author: windows-sdk-content
description: Retrieves the specified file screen.
old-location: fsrm\ifsrmfilescreenmanager_getfilescreen.htm
tech.root: fsrm
ms.assetid: 9af0d9a7-80a2-4cc8-a703-c1af8ac5b7c9
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: FsrmFileScreenManager class [File Server Resource Manager],GetFileScreen method, GetFileScreen, GetFileScreen method [File Server Resource Manager], GetFileScreen method [File Server Resource Manager],FsrmFileScreenManager class, GetFileScreen method [File Server Resource Manager],IFsrmFileScreenManager interface, IFsrmFileScreenManager interface [File Server Resource Manager],GetFileScreen method, IFsrmFileScreenManager.GetFileScreen, IFsrmFileScreenManager::GetFileScreen, fs.ifsrmfilescreenmanager_getfilescreen, fsrm.ifsrmfilescreenmanager_getfilescreen, fsrmscreen/IFsrmFileScreenManager::GetFileScreen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fsrmscreen.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileScreenManager.GetFileScreen
 - FsrmFileScreenManager.GetFileScreen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileScreenManager::GetFileScreen


## -description


Retrieves the specified file screen.


## -parameters




### -param path [in]

The local directory path associated with the file screen that you want to retrieve. The path is limited to 260 characters.


### -param fileScreen [out]

An <a href="https://msdn.microsoft.com/69b831a1-c935-4de0-b222-009bafc45ec5">IFsrmFileScreen</a> interface to the file screen.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/82ff65fa-2e82-4f07-bdd4-e3b01d184c16">FsrmFileScreenManager</a>



<a href="https://msdn.microsoft.com/a0cea95d-5839-41a2-91b9-da8e13030682">IFsrmFileScreenManager</a>
 

 

