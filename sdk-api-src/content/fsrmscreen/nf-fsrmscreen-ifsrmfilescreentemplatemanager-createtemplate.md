---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.CreateTemplate
title: IFsrmFileScreenTemplateManager::CreateTemplate (fsrmscreen.h)
description: Creates a file screen template object.
helpviewer_keywords: ["CreateTemplate","CreateTemplate method [File Server Resource Manager]","CreateTemplate method [File Server Resource Manager]","FsrmFileScreenTemplateManager class","CreateTemplate method [File Server Resource Manager]","IFsrmFileScreenTemplateManager interface","FsrmFileScreenTemplateManager class [File Server Resource Manager]","CreateTemplate method","IFsrmFileScreenTemplateManager interface [File Server Resource Manager]","CreateTemplate method","IFsrmFileScreenTemplateManager.CreateTemplate","IFsrmFileScreenTemplateManager::CreateTemplate","fs.ifsrmfilescreentemplatemanager_createtemplate","fsrm.ifsrmfilescreentemplatemanager_createtemplate","fsrmscreen/IFsrmFileScreenTemplateManager::CreateTemplate"]
old-location: fsrm\ifsrmfilescreentemplatemanager_createtemplate.htm
tech.root: fsrm
ms.assetid: 3d654dee-2a27-4dc0-8e2b-fba546abe17e
ms.date: 12/05/2018
ms.keywords: CreateTemplate, CreateTemplate method [File Server Resource Manager], CreateTemplate method [File Server Resource Manager],FsrmFileScreenTemplateManager class, CreateTemplate method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, FsrmFileScreenTemplateManager class [File Server Resource Manager],CreateTemplate method, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],CreateTemplate method, IFsrmFileScreenTemplateManager.CreateTemplate, IFsrmFileScreenTemplateManager::CreateTemplate, fs.ifsrmfilescreentemplatemanager_createtemplate, fsrm.ifsrmfilescreentemplatemanager_createtemplate, fsrmscreen/IFsrmFileScreenTemplateManager::CreateTemplate
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
 - IFsrmFileScreenTemplateManager::CreateTemplate
 - fsrmscreen/IFsrmFileScreenTemplateManager::CreateTemplate
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
 - IFsrmFileScreenTemplateManager.CreateTemplate
 - FsrmFileScreenTemplateManager.CreateTemplate
---

# IFsrmFileScreenTemplateManager::CreateTemplate


## -description

Creates a file screen template object.

## -parameters

### -param fileScreenTemplate [out]

An <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplate">IFsrmFileScreenTemplate</a> interface to the 
      newly create template. To add the template to FSRM, call the 
      <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmFileScreenTemplate::Commit</a> method.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreentemplatemanager">FsrmFileScreenTemplateManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplatemanager">IFsrmFileScreenTemplateManager</a>