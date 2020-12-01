---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.ImportTemplates
title: IFsrmFileScreenTemplateManager::ImportTemplates (fsrmscreen.h)
description: Imports the specified file screen templates from an XML string.
helpviewer_keywords: ["FsrmFileScreenTemplateManager class [File Server Resource Manager]","ImportTemplates method","IFsrmFileScreenTemplateManager interface [File Server Resource Manager]","ImportTemplates method","IFsrmFileScreenTemplateManager.ImportTemplates","IFsrmFileScreenTemplateManager::ImportTemplates","ImportTemplates","ImportTemplates method [File Server Resource Manager]","ImportTemplates method [File Server Resource Manager]","FsrmFileScreenTemplateManager class","ImportTemplates method [File Server Resource Manager]","IFsrmFileScreenTemplateManager interface","fs.ifsrmfilescreentemplatemanager_importtemplates","fsrm.ifsrmfilescreentemplatemanager_importtemplates","fsrmscreen/IFsrmFileScreenTemplateManager::ImportTemplates"]
old-location: fsrm\ifsrmfilescreentemplatemanager_importtemplates.htm
tech.root: fsrm
ms.assetid: 0660a1cb-904e-4ed0-bbc8-9903e8848f4e
ms.date: 12/05/2018
ms.keywords: FsrmFileScreenTemplateManager class [File Server Resource Manager],ImportTemplates method, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],ImportTemplates method, IFsrmFileScreenTemplateManager.ImportTemplates, IFsrmFileScreenTemplateManager::ImportTemplates, ImportTemplates, ImportTemplates method [File Server Resource Manager], ImportTemplates method [File Server Resource Manager],FsrmFileScreenTemplateManager class, ImportTemplates method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, fs.ifsrmfilescreentemplatemanager_importtemplates, fsrm.ifsrmfilescreentemplatemanager_importtemplates, fsrmscreen/IFsrmFileScreenTemplateManager::ImportTemplates
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
 - IFsrmFileScreenTemplateManager::ImportTemplates
 - fsrmscreen/IFsrmFileScreenTemplateManager::ImportTemplates
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
 - IFsrmFileScreenTemplateManager.ImportTemplates
 - FsrmFileScreenTemplateManager.ImportTemplates
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

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface that contains a collection of file screen templates.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplateimported">IFsrmFileScreenTemplateImported</a> interface.

To add the templates to FSRM, call the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcommittablecollection-commit">IFsrmCommittableCollection::Commit</a> method. To add the templates to FSRM and propagate the changes to objects that were derived from the template, call the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nf-fsrmscreen-ifsrmfilescreentemplate-commitandupdatederived">IFsrmFileScreenTemplateImported::CommitAndUpdateDerived</a> method on each item in the collection.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreentemplatemanager">FsrmFileScreenTemplateManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplatemanager">IFsrmFileScreenTemplateManager</a>