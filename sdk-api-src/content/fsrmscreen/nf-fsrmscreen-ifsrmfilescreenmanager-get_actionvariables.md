---
UID: NF:fsrmscreen.IFsrmFileScreenManager.get_ActionVariables
title: IFsrmFileScreenManager::get_ActionVariables (fsrmscreen.h)
description: Retrieves a list of macros that you can specify in action property values. (IFsrmFileScreenManager.get_ActionVariables)
helpviewer_keywords: ["ActionVariables property [File Server Resource Manager]","ActionVariables property [File Server Resource Manager]","FsrmFileScreenManager class","ActionVariables property [File Server Resource Manager]","IFsrmFileScreenManager interface","FsrmFileScreenManager class [File Server Resource Manager]","ActionVariables property","IFsrmFileScreenManager interface [File Server Resource Manager]","ActionVariables property","IFsrmFileScreenManager.ActionVariables","IFsrmFileScreenManager.get_ActionVariables","IFsrmFileScreenManager::ActionVariables","IFsrmFileScreenManager::get_ActionVariables","fs.ifsrmfilescreenmanager_actionvariables","fsrm.ifsrmfilescreenmanager_actionvariables","fsrmscreen/IFsrmFileScreenManager::ActionVariables","fsrmscreen/IFsrmFileScreenManager::get_ActionVariables","get_ActionVariables"]
old-location: fsrm\ifsrmfilescreenmanager_actionvariables.htm
tech.root: fsrm
ms.assetid: 70bb9e51-cd32-45cd-94b4-7018397e8f77
ms.date: 12/05/2018
ms.keywords: ActionVariables property [File Server Resource Manager], ActionVariables property [File Server Resource Manager],FsrmFileScreenManager class, ActionVariables property [File Server Resource Manager],IFsrmFileScreenManager interface, FsrmFileScreenManager class [File Server Resource Manager],ActionVariables property, IFsrmFileScreenManager interface [File Server Resource Manager],ActionVariables property, IFsrmFileScreenManager.ActionVariables, IFsrmFileScreenManager.get_ActionVariables, IFsrmFileScreenManager::ActionVariables, IFsrmFileScreenManager::get_ActionVariables, fs.ifsrmfilescreenmanager_actionvariables, fsrm.ifsrmfilescreenmanager_actionvariables, fsrmscreen/IFsrmFileScreenManager::ActionVariables, fsrmscreen/IFsrmFileScreenManager::get_ActionVariables, get_ActionVariables
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
 - IFsrmFileScreenManager::get_ActionVariables
 - fsrmscreen/IFsrmFileScreenManager::get_ActionVariables
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
 - IFsrmFileScreenManager.ActionVariables
 - IFsrmFileScreenManager.get_ActionVariables
 - FsrmFileScreenManager.ActionVariables
---

# IFsrmFileScreenManager::get_ActionVariables


## -description

Retrieves a  list of macros that you can specify in action property values.

This property is read-only.

## -parameters

## -remarks

FSRM parses the action property for the macros and substitutes the macro string with the values that are 
    specific to the event and computer on which the action occurred.  For example, the following shows how you can 
    format the message text for email: 
    "User [Source Io Owner] has reached the quota limit for quota on [Quota Path] on server [Server]. The quota limit is [Quota Limit MB] MB and the current usage is [Quota Used MB] MB ([Quota Used Percent]% of limit)."

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmfilescreenmanager">FsrmFileScreenManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmscreen/nn-fsrmscreen-ifsrmfilescreenmanager">IFsrmFileScreenManager</a>
