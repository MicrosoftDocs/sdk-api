---
UID: NF:fsrmscreen.IFsrmFileScreenTemplateManager.EnumTemplates
title: IFsrmFileScreenTemplateManager::EnumTemplates (fsrmscreen.h)
description: Enumerates the file screen templates on the server.
helpviewer_keywords: ["EnumTemplates","EnumTemplates method [File Server Resource Manager]","EnumTemplates method [File Server Resource Manager]","FsrmFileScreenTemplateManager class","EnumTemplates method [File Server Resource Manager]","IFsrmFileScreenTemplateManager interface","FsrmFileScreenTemplateManager class [File Server Resource Manager]","EnumTemplates method","IFsrmFileScreenTemplateManager interface [File Server Resource Manager]","EnumTemplates method","IFsrmFileScreenTemplateManager.EnumTemplates","IFsrmFileScreenTemplateManager::EnumTemplates","fs.ifsrmfilescreentemplatemanager_enumtemplates","fsrm.ifsrmfilescreentemplatemanager_enumtemplates","fsrmscreen/IFsrmFileScreenTemplateManager::EnumTemplates"]
old-location: fsrm\ifsrmfilescreentemplatemanager_enumtemplates.htm
tech.root: fsrm
ms.assetid: 5bfb82f9-50a5-4266-956d-f99e2982a6a5
ms.date: 12/05/2018
ms.keywords: EnumTemplates, EnumTemplates method [File Server Resource Manager], EnumTemplates method [File Server Resource Manager],FsrmFileScreenTemplateManager class, EnumTemplates method [File Server Resource Manager],IFsrmFileScreenTemplateManager interface, FsrmFileScreenTemplateManager class [File Server Resource Manager],EnumTemplates method, IFsrmFileScreenTemplateManager interface [File Server Resource Manager],EnumTemplates method, IFsrmFileScreenTemplateManager.EnumTemplates, IFsrmFileScreenTemplateManager::EnumTemplates, fs.ifsrmfilescreentemplatemanager_enumtemplates, fsrm.ifsrmfilescreentemplatemanager_enumtemplates, fsrmscreen/IFsrmFileScreenTemplateManager::EnumTemplates
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
 - IFsrmFileScreenTemplateManager::EnumTemplates
 - fsrmscreen/IFsrmFileScreenTemplateManager::EnumTemplates
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
 - IFsrmFileScreenTemplateManager.EnumTemplates
 - FsrmFileScreenTemplateManager.EnumTemplates
---

# IFsrmFileScreenTemplateManager::EnumTemplates


## -description

Enumerates the file screen templates on the server.

## -parameters

### -param options [in]

The options to use when enumerating the file screen templates. For possible values, see the <a href="/windows/desktop/api/fsrmenums/ne-fsrmenums-fsrmenumoptions">FsrmEnumOptions</a> enumeration.

### -param fileScreenTemplates [out]

An <a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmcommittablecollection">IFsrmCommittableCollection</a> interface that contains a collection of file screen templates.

Each item of the collection is a <b>VARIANT</b> of type <b>VT_DISPATCH</b>. Query the <b>pdispVal</b> member of the variant for the <a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplate">IFsrmFileScreenTemplate</a> interface.

## -returns

The method returns the following return values.

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreentemplatemanager">FsrmFileScreenTemplateManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreentemplatemanager">IFsrmFileScreenTemplateManager</a>