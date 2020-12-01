---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.ExportTemplates
title: IFsrmFileScreenTemplateManager::ExportTemplates (fsrmscreen.h)
description: Exports the templates as an XML string.
helpviewer_keywords: ["ExportTemplates","ExportTemplates method [File Server Resource Manager]","ExportTemplates method [File Server Resource Manager]","FsrmFileScreenTemplateManager class","ExportTemplates method [File Server Resource Manager]","IFsrmFileScreenTemplateManager interface","FsrmFileScreenTemplateManager class [File Server Resource Manager]","ExportTemplates method","IFsrmFileScreenTemplateManager interface [File Server Resource Manager]","ExportTemplates method","IFsrmFileScreenTemplateManager.ExportTemplates","IFsrmFileScreenTemplateManager::ExportTemplates","fs.ifsrmfilescreentemplatemanager_exporttemplates","fsrm.ifsrmfilescreentemplatemanager_exporttemplates","fsrmscreen/IFsrmFileScreenTemplateManager::ExportTemplates"]
old-location: fsrm\ifsrmfilescreentemplatemanager_exporttemplates.htm
tech.root: fsrm
ms.assetid: 27a0141d-0906-400e-bd5f-81da67a3c501
ms.date: 12/05/2018
ms.keywords: ExportTemplates, ExportTemplates method [File Server Resource Manager], ExportTemplates method [File Server Resource Manager],FsrmFileScreenTemplateManager class, ExportTemplates method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, FsrmFileScreenTemplateManager class [File Server Resource Manager],ExportTemplates method, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],ExportTemplates method, IFsrmFileScreenTemplateManager.ExportTemplates, IFsrmFileScreenTemplateManager::ExportTemplates, fs.ifsrmfilescreentemplatemanager_exporttemplates, fsrm.ifsrmfilescreentemplatemanager_exporttemplates, fsrmscreen/IFsrmFileScreenTemplateManager::ExportTemplates
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFsrmFileScreenTemplateManager::ExportTemplates
 - fsrmscreen/IFsrmFileScreenTemplateManager::ExportTemplates
dev_langs:
 - c++
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

Typically, you use this method to save the templates to a file. You can then copy the file to another computer and call the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplatemanager-importtemplates">IFsrmFileScreenTemplateManager::ImportTemplates</a> method to import the templates.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreentemplatemanager">FsrmFileScreenTemplateManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplatemanager">IFsrmFileScreenTemplateManager</a>