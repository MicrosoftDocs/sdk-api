---
UID: NF:fsrmpipeline.IFsrmStorageModuleDefinition.put_UpdatesFileContent
title: IFsrmStorageModuleDefinition::put_UpdatesFileContent (fsrmpipeline.h)
author: windows-sdk-content
description: Determines whether the module updates the contents of the file.
old-location: fsrm\ifsrmstoragemoduledefinition_updatesfilecontent.htm
tech.root: fsrm
ms.assetid: 461befff-0bb4-44a2-9c37-e9a8fb1b080f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFsrmStorageModuleDefinition interface [File Server Resource Manager],UpdatesFileContent property, IFsrmStorageModuleDefinition.UpdatesFileContent, IFsrmStorageModuleDefinition.put_UpdatesFileContent, IFsrmStorageModuleDefinition::UpdatesFileContent, IFsrmStorageModuleDefinition::get_UpdatesFileContent, IFsrmStorageModuleDefinition::put_UpdatesFileContent, UpdatesFileContent property [File Server Resource Manager], UpdatesFileContent property [File Server Resource Manager],IFsrmStorageModuleDefinition interface, fs.ifsrmstoragemoduledefinition_updatesfilecontent, fsrm.ifsrmstoragemoduledefinition_updatesfilecontent, fsrmpipeline/IFsrmStorageModuleDefinition::UpdatesFileContent, fsrmpipeline/IFsrmStorageModuleDefinition::get_UpdatesFileContent, fsrmpipeline/IFsrmStorageModuleDefinition::put_UpdatesFileContent, put_UpdatesFileContent
ms.topic: method
req.header: fsrmpipeline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
 - IFsrmStorageModuleDefinition.UpdatesFileContent
 - IFsrmStorageModuleDefinition.get_UpdatesFileContent
 - IFsrmStorageModuleDefinition.put_UpdatesFileContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmStorageModuleDefinition::put_UpdatesFileContent


## -description


Determines whether the module updates the contents of the file.

This property is read/write.


## -parameters


## -remarks



Setting this property to <b>VARIANT_TRUE</b> does not require that the 
    <a href="https://msdn.microsoft.com/4c4aaacf-d121-412c-9152-5787f351c19c">IFsrmStorageModuleDefinition::StorageType</a> 
    property to be set to <b>FsrmStorageModuleType_InFile</b>. For example, you can set this 
    property to <b>VARIANT_TRUE</b> if you need to update the file to let another process know that 
    you have processed the file.




## -see-also




<a href="https://msdn.microsoft.com/68ecb5e6-61b0-488f-b6bb-181f253de70e">IFsrmStorageModuleDefinition</a>
 

 

