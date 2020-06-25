---
UID: NF:fsrmreports.IFsrmFileManagementJobManager.get_ActionVariables
title: IFsrmFileManagementJobManager::get_ActionVariables (fsrmreports.h)
description: Retrieves a list of macros that you can specify in action property values.
helpviewer_keywords: ["ActionVariables property [File Server Resource Manager]","ActionVariables property [File Server Resource Manager]","FsrmFileManagementJobManager class","ActionVariables property [File Server Resource Manager]","IFsrmFileManagementJobManager interface","FsrmFileManagementJobManager class [File Server Resource Manager]","ActionVariables property","IFsrmFileManagementJobManager interface [File Server Resource Manager]","ActionVariables property","IFsrmFileManagementJobManager.ActionVariables","IFsrmFileManagementJobManager.get_ActionVariables","IFsrmFileManagementJobManager::ActionVariables","IFsrmFileManagementJobManager::get_ActionVariables","fs.ifsrmfilemanagementjobmanager_actionvariables","fsrm.ifsrmfilemanagementjobmanager_actionvariables","fsrmreports/IFsrmFileManagementJobManager::ActionVariables","fsrmreports/IFsrmFileManagementJobManager::get_ActionVariables","get_ActionVariables"]
old-location: fsrm\ifsrmfilemanagementjobmanager_actionvariables.htm
tech.root: fsrm
ms.assetid: 222c826f-0ade-4e5d-be2e-5c0dfa8758d0
ms.date: 12/05/2018
ms.keywords: ActionVariables property [File Server Resource Manager], ActionVariables property [File Server Resource Manager],FsrmFileManagementJobManager class, ActionVariables property [File Server Resource Manager],IFsrmFileManagementJobManager interface, FsrmFileManagementJobManager class [File Server Resource Manager],ActionVariables property, IFsrmFileManagementJobManager interface [File Server Resource Manager],ActionVariables property, IFsrmFileManagementJobManager.ActionVariables, IFsrmFileManagementJobManager.get_ActionVariables, IFsrmFileManagementJobManager::ActionVariables, IFsrmFileManagementJobManager::get_ActionVariables, fs.ifsrmfilemanagementjobmanager_actionvariables, fsrm.ifsrmfilemanagementjobmanager_actionvariables, fsrmreports/IFsrmFileManagementJobManager::ActionVariables, fsrmreports/IFsrmFileManagementJobManager::get_ActionVariables, get_ActionVariables
f1_keywords:
- fsrmreports/IFsrmFileManagementJobManager.ActionVariables
dev_langs:
- c++
req.header: fsrmreports.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
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
- IFsrmFileManagementJobManager.ActionVariables
- IFsrmFileManagementJobManager.get_ActionVariables
- FsrmFileManagementJobManager.ActionVariables
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFsrmFileManagementJobManager::get_ActionVariables


## -description


Retrieves a  list of macros that you can specify in action property values.

This property is read-only.


## -parameters


## -remarks



FSRM parses the action property for the macros and substitutes the macro string with the values that are specific to the event and computer on which the action occurred.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fsrm/fsrmfilemanagementjobmanager">FsrmFileManagementJobManager</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/fsrmreports/nn-fsrmreports-ifsrmfilemanagementjobmanager">IFsrmFileManagementJobManager</a>
 

 

