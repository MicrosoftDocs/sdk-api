---
UID: NF:fsrmscreen.IFsrmFileScreenManager.CreateFileScreenException
title: IFsrmFileScreenManager::CreateFileScreenException
author: windows-sdk-content
description: Creates a file screen exception object.
old-location: fsrm\ifsrmfilescreenmanager_createfilescreenexception.htm
old-project: Fsrm
ms.assetid: b2a15f69-49fb-46fd-9219-aa970c9eb042
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CreateFileScreenException, CreateFileScreenException method [File Server Resource Manager], CreateFileScreenException method [File Server Resource Manager],FsrmFileScreenManager class, CreateFileScreenException method [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],CreateFileScreenException method, IFsrmFileScreenManager interface [File Server Resource Manager],CreateFileScreenException method, IFsrmFileScreenManager.CreateFileScreenException, IFsrmFileScreenManager::CreateFileScreenException, fs.ifsrmfilescreenmanager_createfilescreenexception, fsrm.ifsrmfilescreenmanager_createfilescreenexception, fsrmscreen/IFsrmFileScreenManager::CreateFileScreenException
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FsrmTemplateApplyOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmFileScreenManager.CreateFileScreenException
 - FsrmFileScreenManager.CreateFileScreenException
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenManager::CreateFileScreenException


## -description


Creates a file screen exception object.


## -parameters




### -param path [in]

The local directory path to which the file screen exception applies. The path is limited to 260 characters.


### -param fileScreenException [out]

An <a href="https://msdn.microsoft.com/188e76dd-6df6-412f-8d51-fc727075de80">IFsrmFileScreenException</a> interface of the newly created file screen exception. To add the exception to FSRM, call <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileScreenException::Commit</a> method.


## -returns



The method returns the following return values.




## -remarks



You can use the exception to allow files to be saved in a directory when a file screen would otherwise prevent it. For example, if P:\<i>directory</i> contains a file screen that blocks *.mp3, you could create an exception that allows MP3 files on P:\<i>directory</i>\<i>subdirectory</i>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/a046f092-5b6d-452d-826b-fd4b83c774fb">Defining a File Screen Exception</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/82ff65fa-2e82-4f07-bdd4-e3b01d184c16">FsrmFileScreenManager</a>



<a href="https://msdn.microsoft.com/a0cea95d-5839-41a2-91b9-da8e13030682">IFsrmFileScreenManager</a>
 

 

