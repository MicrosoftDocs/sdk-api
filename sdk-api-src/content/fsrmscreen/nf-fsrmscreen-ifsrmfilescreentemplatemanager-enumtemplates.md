---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.EnumTemplates
title: IFsrmFileScreenTemplateManager::EnumTemplates
author: windows-sdk-content
description: Enumerates the file screen templates on the server.
old-location: fsrm\ifsrmfilescreentemplatemanager_enumtemplates.htm
tech.root: fsrm
ms.assetid: 5bfb82f9-50a5-4266-956d-f99e2982a6a5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: EnumTemplates, EnumTemplates method [File Server Resource Manager], EnumTemplates method [File Server Resource Manager],FsrmFileScreenTemplateManager class, EnumTemplates method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, FsrmFileScreenTemplateManager class [File Server Resource Manager],EnumTemplates method, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],EnumTemplates method, IFsrmFileScreenTemplateManager.EnumTemplates, IFsrmFileScreenTemplateManager::EnumTemplates, fs.ifsrmfilescreentemplatemanager_enumtemplates, fsrm.ifsrmfilescreentemplatemanager_enumtemplates, fsrmscreen/IFsrmFileScreenTemplateManager::EnumTemplates
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
 - IFsrmFileScreenTemplateManager.EnumTemplates
 - FsrmFileScreenTemplateManager.EnumTemplates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileScreenTemplateManager::EnumTemplates


## -description


Enumerates the file screen templates on the server.


## -parameters




### -param options [in]

The options to use when enumerating the file screen templates. For possible values, see the <a href="https://msdn.microsoft.com/9c613d0c-c49a-4010-b66f-a63c57d693f7">FsrmEnumOptions</a> enumeration.


### -param fileScreenTemplates [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface that contains a collection of file screen templates.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for the <a href="https://msdn.microsoft.com/c8e612f5-e7cd-45ff-9eaf-9d1674231161">IFsrmFileScreenTemplate</a> interface.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/e736def1-ebfd-4f3e-9729-f8dd46f59516">FsrmFileScreenTemplateManager</a>



<a href="https://msdn.microsoft.com/89577ab3-2648-4b37-9fc0-c64929223a13">IFsrmFileScreenTemplateManager</a>
 

 

