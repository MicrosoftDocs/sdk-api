---
UID: NF:fsrm.IFsrmAction.Delete
title: IFsrmAction::Delete (fsrm.h)
description: Removes the action from the quota or file screen's list of actions.
helpviewer_keywords: ["Delete","Delete method [File Server Resource Manager]","Delete method [File Server Resource Manager]","IFsrmAction interface","IFsrmAction interface [File Server Resource Manager]","Delete method","IFsrmAction.Delete","IFsrmAction::Delete","fs.ifsrmaction_delete","fsrm.ifsrmaction_delete","fsrm/IFsrmAction::Delete"]
old-location: fsrm\ifsrmaction_delete.htm
tech.root: fsrm
ms.assetid: 66d17a40-704d-46e6-b8bb-ae7f80e52fa5
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [File Server Resource Manager], Delete method [File Server Resource Manager],IFsrmAction interface, IFsrmAction interface [File Server Resource Manager],Delete method, IFsrmAction.Delete, IFsrmAction::Delete, fs.ifsrmaction_delete, fsrm.ifsrmaction_delete, fsrm/IFsrmAction::Delete
req.header: fsrm.h
req.include-header: FsrmQuota.h, FsrmScreen.h
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
 - IFsrmAction::Delete
 - fsrm/IFsrmAction::Delete
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
 - IFsrmAction.Delete
---

# IFsrmAction::Delete


## -description

<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="/previous-versions/windows/desktop/fsrm/fsrm-wmi-classes">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmaction">MSFT_FSRMAction</a>,
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjaction">MSFT_FSRMFMJAction</a>, and 
    <a href="/previous-versions/windows/desktop/fsrm/msft-fsrmfmjnotificationaction">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Removes the action from the quota or file screen's list of actions.



## -returns

The method returns the following return values.

## -remarks

Calling the 
    <a href="/previous-versions/windows/desktop/api/fsrmquota/nf-fsrmquota-ifsrmquotabase-deletethreshold">IFsrmQuotaBase::DeleteThreshold</a> method also 
    deletes the actions associated with the threshold.

Note that the actions are not  deleted from the object until you call the object's 
    <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">Commit</a> method. For example, the actions are not deleted 
    from the quota until the <a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmobject-commit">IFsrmQuota::Commit</a> 
    method is called, nor from the file screens until you call the 
    <b>IFsrmFileScreen::Commit</b> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nn-fsrm-ifsrmaction">IFsrmAction</a>
