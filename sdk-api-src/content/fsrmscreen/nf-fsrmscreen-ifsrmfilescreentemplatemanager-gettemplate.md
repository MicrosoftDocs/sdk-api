---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.GetTemplate
title: IFsrmFileScreenTemplateManager::GetTemplate (fsrmscreen.h)
description: Retrieves the specified file screen template.
helpviewer_keywords: ["FsrmFileScreenTemplateManager class [File Server Resource Manager]","GetTemplate method","GetTemplate","GetTemplate method [File Server Resource Manager]","GetTemplate method [File Server Resource Manager]","FsrmFileScreenTemplateManager class","GetTemplate method [File Server Resource Manager]","IFsrmFileScreenTemplateManager interface","IFsrmFileScreenTemplateManager interface [File Server Resource Manager]","GetTemplate method","IFsrmFileScreenTemplateManager.GetTemplate","IFsrmFileScreenTemplateManager::GetTemplate","fs.ifsrmfilescreentemplatemanager_gettemplate","fsrm.ifsrmfilescreentemplatemanager_gettemplate","fsrmscreen/IFsrmFileScreenTemplateManager::GetTemplate"]
old-location: fsrm\ifsrmfilescreentemplatemanager_gettemplate.htm
tech.root: fsrm
ms.assetid: e97149f6-8cf5-433c-a487-799322253e44
ms.date: 12/05/2018
ms.keywords: FsrmFileScreenTemplateManager class [File Server Resource Manager],GetTemplate method, GetTemplate, GetTemplate method [File Server Resource Manager], GetTemplate method [File Server Resource Manager],FsrmFileScreenTemplateManager class, GetTemplate method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],GetTemplate method, IFsrmFileScreenTemplateManager.GetTemplate, IFsrmFileScreenTemplateManager::GetTemplate, fs.ifsrmfilescreentemplatemanager_gettemplate, fsrm.ifsrmfilescreentemplatemanager_gettemplate, fsrmscreen/IFsrmFileScreenTemplateManager::GetTemplate
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
 - IFsrmFileScreenTemplateManager::GetTemplate
 - fsrmscreen/IFsrmFileScreenTemplateManager::GetTemplate
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
 - IFsrmFileScreenTemplateManager.GetTemplate
 - FsrmFileScreenTemplateManager.GetTemplate
---

# IFsrmFileScreenTemplateManager::GetTemplate


## -description

Retrieves the specified file screen template.

## -parameters

### -param name [in]

The name of the file screen template to retrieve. The name is limited to 4,000 characters.

### -param fileScreenTemplate [out]

An <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplate">IFsrmFileScreenTemplate</a> interface to the retrieved template.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreentemplatemanager">FsrmFileScreenTemplateManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplatemanager">IFsrmFileScreenTemplateManager</a>