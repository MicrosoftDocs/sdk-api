---
UID: NF:fsrmquota.IFsrmQuotaManager.get_ActionVariables
title: IFsrmQuotaManager::get_ActionVariables (fsrmquota.h)
description: Retrieves a list of macros that you can specify in action property values. (IFsrmQuotaManagerEx.get_ActionVariables)
helpviewer_keywords: ["ActionVariables property [File Server Resource Manager]","ActionVariables property [File Server Resource Manager]","FsrmQuotaManager class","ActionVariables property [File Server Resource Manager]","IFsrmQuotaManager interface","ActionVariables property [File Server Resource Manager]","IFsrmQuotaManagerEx interface","FsrmQuotaManager class [File Server Resource Manager]","ActionVariables property","IFsrmQuotaManager interface [File Server Resource Manager]","ActionVariables property","IFsrmQuotaManager.ActionVariables","IFsrmQuotaManager.get_ActionVariables","IFsrmQuotaManager::ActionVariables","IFsrmQuotaManager::get_ActionVariables","IFsrmQuotaManagerEx interface [File Server Resource Manager]","ActionVariables property","IFsrmQuotaManagerEx.ActionVariables","IFsrmQuotaManagerEx::get_ActionVariables","fs.ifsrmquotamanager_actionvariables","fsrm.ifsrmquotamanager_actionvariables","fsrmquota/IFsrmQuotaManager::ActionVariables","fsrmquota/IFsrmQuotaManager::get_ActionVariables","fsrmquota/IFsrmQuotaManagerEx::ActionVariables","fsrmquota/IFsrmQuotaManagerEx::get_ActionVariables","get_ActionVariables"]
old-location: fsrm\ifsrmquotamanager_actionvariables.htm
tech.root: fsrm
ms.assetid: e7fe0139-692b-4f88-8411-ffd31d29e40d
ms.date: 12/05/2018
ms.keywords: ActionVariables property [File Server Resource Manager], ActionVariables property [File Server Resource Manager],FsrmQuotaManager class, ActionVariables property [File Server Resource Manager],IFsrmQuotaManager interface, ActionVariables property [File Server Resource Manager],IFsrmQuotaManagerEx interface, FsrmQuotaManager class [File Server Resource Manager],ActionVariables property, IFsrmQuotaManager interface [File Server Resource Manager],ActionVariables property, IFsrmQuotaManager.ActionVariables, IFsrmQuotaManager.get_ActionVariables, IFsrmQuotaManager::ActionVariables, IFsrmQuotaManager::get_ActionVariables, IFsrmQuotaManagerEx interface [File Server Resource Manager],ActionVariables property, IFsrmQuotaManagerEx.ActionVariables, IFsrmQuotaManagerEx::get_ActionVariables, fs.ifsrmquotamanager_actionvariables, fsrm.ifsrmquotamanager_actionvariables, fsrmquota/IFsrmQuotaManager::ActionVariables, fsrmquota/IFsrmQuotaManager::get_ActionVariables, fsrmquota/IFsrmQuotaManagerEx::ActionVariables, fsrmquota/IFsrmQuotaManagerEx::get_ActionVariables, get_ActionVariables
req.header: fsrmquota.h
req.include-header: FsrmQuota.h, FsrmTlb.h
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
 - IFsrmQuotaManager::get_ActionVariables
 - fsrmquota/IFsrmQuotaManager::get_ActionVariables
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
 - IFsrmQuotaManager.ActionVariables
 - IFsrmQuotaManager.get_ActionVariables
 - IFsrmQuotaManagerEx.ActionVariables
 - IFsrmQuotaManagerEx.get_ActionVariables
 - FsrmQuotaManager.ActionVariables
---

# IFsrmQuotaManager::get_ActionVariables


## -description

<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a> class.]

Retrieves a  list of macros that you can specify in action property values.

This property is read-only.

## -parameters

## -remarks

FSRM parses the action property for the macros and substitutes the macro string with the values that are 
    specific to the event and computer on which the action occurred. For example, the following shows how you can 
    format the message text for email: 
    "User [<i>Source Io Owner</i>] has reached the quota limit for quota on [<i>Quota Path</i>] on server [<i>Server</i>]. The quota limit is [<i>Quota Limit MB</i>] MB and the current usage is [<i>Quota Used MB</i>] MB ([<i>Quota Used Percent</i>]% of limit)."

## -see-also

<a href="/previous-versions/windows/desktop/fsrm/fsrmquotamanager">FsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanager">IFsrmQuotaManager</a>



<a href="/previous-versions/windows/desktop/api/fsrmquota/nn-fsrmquota-ifsrmquotamanagerex">IFsrmQuotaManagerEx</a>



<a href="/previous-versions/windows/desktop/fsrm/msft-fsrmquota">MSFT_FSRMQuota</a>
