---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.GetTemplate
title: IFsrmFileScreenTemplateManager::GetTemplate
author: windows-sdk-content
description: Retrieves the specified file screen template.
old-location: fsrm\ifsrmfilescreentemplatemanager_gettemplate.htm
tech.root: fsrm
ms.assetid: e97149f6-8cf5-433c-a487-799322253e44
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FsrmFileScreenTemplateManager class [File Server Resource Manager],GetTemplate method, GetTemplate, GetTemplate method [File Server Resource Manager], GetTemplate method [File Server Resource Manager],FsrmFileScreenTemplateManager class, GetTemplate method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],GetTemplate method, IFsrmFileScreenTemplateManager.GetTemplate, IFsrmFileScreenTemplateManager::GetTemplate, fs.ifsrmfilescreentemplatemanager_gettemplate, fsrm.ifsrmfilescreentemplatemanager_gettemplate, fsrmscreen/IFsrmFileScreenTemplateManager::GetTemplate
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
 - IFsrmFileScreenTemplateManager.GetTemplate
 - FsrmFileScreenTemplateManager.GetTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmFileScreenTemplateManager::GetTemplate


## -description


Retrieves the specified file screen template.


## -parameters




### -param name [in]

The name of the file screen template to retrieve. The name is limited to 4,000 characters.


### -param fileScreenTemplate [out]

An <a href="https://msdn.microsoft.com/c8e612f5-e7cd-45ff-9eaf-9d1674231161">IFsrmFileScreenTemplate</a> interface to the retrieved template.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/e736def1-ebfd-4f3e-9729-f8dd46f59516">FsrmFileScreenTemplateManager</a>



<a href="https://msdn.microsoft.com/89577ab3-2648-4b37-9fc0-c64929223a13">IFsrmFileScreenTemplateManager</a>
 

 

