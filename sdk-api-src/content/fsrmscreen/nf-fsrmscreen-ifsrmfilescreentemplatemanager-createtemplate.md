---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.CreateTemplate
title: IFsrmFileScreenTemplateManager::CreateTemplate
author: windows-sdk-content
description: Creates a file screen template object.
old-location: fsrm\ifsrmfilescreentemplatemanager_createtemplate.htm
old-project: fsrm
ms.assetid: 3d654dee-2a27-4dc0-8e2b-fba546abe17e
ms.author: windowssdkdev
ms.date: 08/01/2018
ms.keywords: CreateTemplate, CreateTemplate method [File Server Resource Manager], CreateTemplate method [File Server Resource Manager],FsrmFileScreenTemplateManager class, CreateTemplate method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, FsrmFileScreenTemplateManager class [File Server Resource Manager],CreateTemplate method, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],CreateTemplate method, IFsrmFileScreenTemplateManager.CreateTemplate, IFsrmFileScreenTemplateManager::CreateTemplate, fs.ifsrmfilescreentemplatemanager_createtemplate, fsrm.ifsrmfilescreentemplatemanager_createtemplate, fsrmscreen/IFsrmFileScreenTemplateManager::CreateTemplate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: fsrmscreen.h
req.include-header: 
req.redist: 
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
 - IFsrmFileScreenTemplateManager.CreateTemplate
 - FsrmFileScreenTemplateManager.CreateTemplate
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenTemplateManager::CreateTemplate


## -description


Creates a file screen template object.


## -parameters




### -param fileScreenTemplate [out]

An <a href="https://msdn.microsoft.com/c8e612f5-e7cd-45ff-9eaf-9d1674231161">IFsrmFileScreenTemplate</a> interface to the 
      newly create template. To add the template to FSRM, call the 
      <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmFileScreenTemplate::Commit</a> method.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/e736def1-ebfd-4f3e-9729-f8dd46f59516">FsrmFileScreenTemplateManager</a>



<a href="https://msdn.microsoft.com/89577ab3-2648-4b37-9fc0-c64929223a13">IFsrmFileScreenTemplateManager</a>
 

 

