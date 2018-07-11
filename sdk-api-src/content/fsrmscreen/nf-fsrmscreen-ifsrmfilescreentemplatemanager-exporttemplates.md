---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.ExportTemplates
title: IFsrmFileScreenTemplateManager::ExportTemplates
author: windows-sdk-content
description: Exports the templates as an XML string.
old-location: fsrm\ifsrmfilescreentemplatemanager_exporttemplates.htm
old-project: fsrm
ms.assetid: 27a0141d-0906-400e-bd5f-81da67a3c501
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: ExportTemplates, ExportTemplates method [File Server Resource Manager], ExportTemplates method [File Server Resource Manager],FsrmFileScreenTemplateManager class, ExportTemplates method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, FsrmFileScreenTemplateManager class [File Server Resource Manager],ExportTemplates method, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],ExportTemplates method, IFsrmFileScreenTemplateManager.ExportTemplates, IFsrmFileScreenTemplateManager::ExportTemplates, fs.ifsrmfilescreentemplatemanager_exporttemplates, fsrm.ifsrmfilescreentemplatemanager_exporttemplates, fsrmscreen/IFsrmFileScreenTemplateManager::ExportTemplates
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
 - IFsrmFileScreenTemplateManager.ExportTemplates
 - FsrmFileScreenTemplateManager.ExportTemplates
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenTemplateManager::ExportTemplates


## -description


Exports the templates as an XML string.


## -parameters




### -param fileScreenTemplateNamesArray [in]

A variant that contains the names of the file screen templates to export. If <b>NULL</b>, the method exports all file screens.


### -param serializedFileScreenTemplates [out]

The specified templates in XML format.


## -returns



The method returns the following return values.




## -remarks



Typically, you use this method to save the templates to a file. You can then copy the file to another computer and call the <a href="https://msdn.microsoft.com/0660a1cb-904e-4ed0-bbc8-9903e8848f4e">IFsrmFileScreenTemplateManager::ImportTemplates</a> method to import the templates.




## -see-also




<a href="https://msdn.microsoft.com/e736def1-ebfd-4f3e-9729-f8dd46f59516">FsrmFileScreenTemplateManager</a>



<a href="https://msdn.microsoft.com/89577ab3-2648-4b37-9fc0-c64929223a13">IFsrmFileScreenTemplateManager</a>
 

 

