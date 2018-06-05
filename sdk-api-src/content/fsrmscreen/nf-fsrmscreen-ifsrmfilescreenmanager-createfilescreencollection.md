---
UID: NF:fsrmscreen.IFsrmFileScreenManager.CreateFileScreenCollection
title: IFsrmFileScreenManager::CreateFileScreenCollection
author: windows-sdk-content
description: Creates an empty collection to which you can add file screens.
old-location: fsrm\ifsrmfilescreenmanager_createfilescreencollection.htm
old-project: Fsrm
ms.assetid: 4adce5d6-8be6-477b-8dab-d437163b4449
ms.author: windowssdkdev
ms.date: 04/18/2018
ms.keywords: CreateFileScreenCollection, CreateFileScreenCollection method [File Server Resource Manager], CreateFileScreenCollection method [File Server Resource Manager],FsrmFileScreenManager class, CreateFileScreenCollection method [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],CreateFileScreenCollection method, IFsrmFileScreenManager interface [File Server Resource Manager],CreateFileScreenCollection method, IFsrmFileScreenManager.CreateFileScreenCollection, IFsrmFileScreenManager::CreateFileScreenCollection, fs.ifsrmfilescreenmanager_createfilescreencollection, fsrm.ifsrmfilescreenmanager_createfilescreencollection, fsrmscreen/IFsrmFileScreenManager::CreateFileScreenCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmscreen.h
req.include-header: FsrmQuota.h
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmFileScreenManager.CreateFileScreenCollection
-	FsrmFileScreenManager.CreateFileScreenCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenManager::CreateFileScreenCollection


## -description


Creates an empty collection to which you can add file screens.


## -parameters




### -param collection [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface to the newly created collection. To add an object to the collection, call the <a href="https://msdn.microsoft.com/916f01de-c87c-450c-859a-c349a165f91d">IFsrmMutableCollection::Add</a> method.


## -returns



The method returns the following return values.




## -remarks



After adding the file screens to the collection, call the <a href="https://msdn.microsoft.com/844cb2a5-8526-434b-af22-b1bf856ed6af">IFsrmCommittableCollection::Commit</a> method.




## -see-also




<a href="https://msdn.microsoft.com/82ff65fa-2e82-4f07-bdd4-e3b01d184c16">FsrmFileScreenManager</a>



<a href="https://msdn.microsoft.com/a0cea95d-5839-41a2-91b9-da8e13030682">IFsrmFileScreenManager</a>
 

 

