---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.ImportTemplates
title: IFsrmFileScreenTemplateManager::ImportTemplates
author: windows-sdk-content
description: Imports the specified file screen templates from an XML string.
old-location: fsrm\ifsrmfilescreentemplatemanager_importtemplates.htm
old-project: Fsrm
ms.assetid: 0660a1cb-904e-4ed0-bbc8-9903e8848f4e
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: FsrmFileScreenTemplateManager class [File Server Resource Manager],ImportTemplates method, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],ImportTemplates method, IFsrmFileScreenTemplateManager.ImportTemplates, IFsrmFileScreenTemplateManager::ImportTemplates, ImportTemplates, ImportTemplates method [File Server Resource Manager], ImportTemplates method [File Server Resource Manager],FsrmFileScreenTemplateManager class, ImportTemplates method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, fs.ifsrmfilescreentemplatemanager_importtemplates, fsrm.ifsrmfilescreentemplatemanager_importtemplates, fsrmscreen/IFsrmFileScreenTemplateManager::ImportTemplates
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
 - IFsrmFileScreenTemplateManager.ImportTemplates
 - FsrmFileScreenTemplateManager.ImportTemplates
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmFileScreenTemplateManager::ImportTemplates


## -description


Imports the specified file screen templates from an XML string.


## -parameters




### -param serializedFileScreenTemplates [in]

An XML string that represents one or more file screen templates.


### -param fileScreenTemplateNamesArray [in]

A <b>VARIANT</b> that contains a <b>SAFEARRAY</b> of the names of the templates to import. If <b>NULL</b>, the method imports all templates.


### -param fileScreenTemplates [out]

An <a href="https://msdn.microsoft.com/ef4678b4-e6b0-4044-ba11-7a3ae01ad2c7">IFsrmCommittableCollection</a> interface that contains a collection of file screen templates.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for the <a href="https://msdn.microsoft.com/9e3c3d05-298d-4373-abd2-21de9770e85c">IFsrmFileScreenTemplateImported</a> interface.

To add the templates to FSRM, call the <a href="https://msdn.microsoft.com/844cb2a5-8526-434b-af22-b1bf856ed6af">IFsrmCommittableCollection::Commit</a> method. To add the templates to FSRM and propagate the changes to objects that were derived from the template, call the <a href="https://msdn.microsoft.com/6b50a93f-f6f0-4ab4-a4a3-3995b721c5d7">IFsrmFileScreenTemplateImported::CommitAndUpdateDerived</a> method on each item in the collection.


## -returns



The method returns the following return values.




## -see-also




<a href="https://msdn.microsoft.com/e736def1-ebfd-4f3e-9729-f8dd46f59516">FsrmFileScreenTemplateManager</a>



<a href="https://msdn.microsoft.com/89577ab3-2648-4b37-9fc0-c64929223a13">IFsrmFileScreenTemplateManager</a>
 

 

