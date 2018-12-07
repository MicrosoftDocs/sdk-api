---
UID: NF:fsrmscreen.IFsrmFileScreenManager.CreateFileScreen
title: IFsrmFileScreenManager::CreateFileScreen
author: windows-sdk-content
description: Creates a file screen object.
old-location: fsrm\ifsrmfilescreenmanager_createfilescreen.htm
tech.root: fsrm
ms.assetid: 5e35c647-2b5a-486b-b8c5-0bc25bd313ad
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateFileScreen, CreateFileScreen method [File Server Resource Manager], CreateFileScreen method [File Server Resource Manager],FsrmFileScreenManager class, CreateFileScreen method [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],CreateFileScreen method, IFsrmFileScreenManager interface [File Server Resource Manager],CreateFileScreen method, IFsrmFileScreenManager.CreateFileScreen, IFsrmFileScreenManager::CreateFileScreen, fs.ifsrmfilescreenmanager_createfilescreen, fsrm.ifsrmfilescreenmanager_createfilescreen, fsrmscreen/IFsrmFileScreenManager::CreateFileScreen
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
 - IFsrmFileScreenManager.CreateFileScreen
 - FsrmFileScreenManager.CreateFileScreen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileScreenManager::CreateFileScreen


## -description


Creates a file screen object.


## -parameters




### -param path [in]

The local directory path to which the file screen applies. The string is limited to 260 characters.


### -param fileScreen [out]

An <a href="https://msdn.microsoft.com/69b831a1-c935-4de0-b222-009bafc45ec5">IFsrmFileScreen</a> interface of the newly created file screen. To add the file screen to FSRM, call the <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileScreen::Commit</a> method.


## -returns



The method returns the following return values.




## -remarks



The screen applies to the directory and all its subdirectories (recursively). For example, a screen on P:\<i>directory</i> that blocks *.mp3 also blocks MP3 files on P:\<i>directory</i>\<i>subdirectory</i>.

If you create a file screen on P:\<i>directory</i>\<i>subdirectory</i>, the screen that you created on P:\<i>directory</i> still applies to P:\<i>directory</i>\<i>subdirectory</i>. If you do not want the screen on P:\<i>directory</i> to  apply to P:\<i>directory</i>\<i>subdirectory</i>, you need to create a <a href="https://msdn.microsoft.com/b2a15f69-49fb-46fd-9219-aa970c9eb042">file screen exception</a>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/1b5227e7-4272-4e23-ba55-d6161e2987bc">Defining a File Screen</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/82ff65fa-2e82-4f07-bdd4-e3b01d184c16">FsrmFileScreenManager</a>



<a href="https://msdn.microsoft.com/a0cea95d-5839-41a2-91b9-da8e13030682">IFsrmFileScreenManager</a>
 

 

