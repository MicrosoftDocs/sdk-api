---
UID: NF:fsrm.IFsrmAction.Delete
title: IFsrmAction::Delete
author: windows-sdk-content
description: Removes the action from the quota or file screen's list of actions.
old-location: fsrm\ifsrmaction_delete.htm
tech.root: Fsrm
ms.assetid: 66d17a40-704d-46e6-b8bb-ae7f80e52fa5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Delete, Delete method [File Server Resource Manager], Delete method [File Server Resource Manager],IFsrmAction interface, IFsrmAction interface [File Server Resource Manager],Delete method, IFsrmAction.Delete, IFsrmAction::Delete, fs.ifsrmaction_delete, fsrm.ifsrmaction_delete, fsrm/IFsrmAction::Delete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmAction.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmAction::Delete


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/55bacec3-c6d1-40ce-902c-8c38eb9a9e7b">MSFT_FSRMAction</a>,
    <a href="https://msdn.microsoft.com/f396e2cb-cfe0-4b4f-bd01-7814a83fb133">MSFT_FSRMFMJAction</a>, and 
    <a href="https://msdn.microsoft.com/17ddc76c-1aba-4eaf-aab0-034933c6052e">MSFT_FSRMFMJNotificationAction</a> 
    classes.]

Removes the action from the quota or file screen's list of actions.


## -parameters






## -returns



The method returns the following return values.




## -remarks



Calling the 
    <a href="https://msdn.microsoft.com/6f6ace15-05aa-4276-88eb-3a4315b3b51c">IFsrmQuotaBase::DeleteThreshold</a> method also 
    deletes the actions associated with the threshold.

Note that the actions are not  deleted from the object until you call the object's 
    <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">Commit</a> method. For example, the actions are not deleted 
    from the quota until the <a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">IFsrmQuota::Commit</a> 
    method is called, nor from the file screens until you call the 
    <b>IFsrmFileScreen::Commit</b> method.




## -see-also




<a href="https://msdn.microsoft.com/81bfae1d-7d09-4ddc-9669-1da40dc72fd4">IFsrmAction</a>
 

 

