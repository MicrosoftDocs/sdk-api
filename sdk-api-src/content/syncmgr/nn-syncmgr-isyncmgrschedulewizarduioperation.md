---
UID: NN:syncmgr.ISyncMgrScheduleWizardUIOperation
title: ISyncMgrScheduleWizardUIOperation (syncmgr.h)
description: Exposes a method that allows a handler to display the sync schedule wizard for the handler.
helpviewer_keywords: ["ISyncMgrScheduleWizardUIOperation","ISyncMgrScheduleWizardUIOperation interface [Windows Shell]","ISyncMgrScheduleWizardUIOperation interface [Windows Shell]","described","_shell_ISyncMgrScheduleWizardUIOperation","shell.ISyncMgrScheduleWizardUIOperation","syncmgr/ISyncMgrScheduleWizardUIOperation"]
old-location: shell\ISyncMgrScheduleWizardUIOperation.htm
tech.root: shell
ms.assetid: dcbe22fb-624f-4784-b1c3-5c463d6502a3
ms.date: 12/05/2018
ms.keywords: ISyncMgrScheduleWizardUIOperation, ISyncMgrScheduleWizardUIOperation interface [Windows Shell], ISyncMgrScheduleWizardUIOperation interface [Windows Shell],described, _shell_ISyncMgrScheduleWizardUIOperation, shell.ISyncMgrScheduleWizardUIOperation, syncmgr/ISyncMgrScheduleWizardUIOperation
f1_keywords:
- syncmgr/ISyncMgrScheduleWizardUIOperation
dev_langs:
- c++
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Syncmgr.h
api_name:
- ISyncMgrScheduleWizardUIOperation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrScheduleWizardUIOperation interface


## -description


Exposes a method that allows a handler to display the sync schedule wizard for the handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrScheduleWizardUIOperation</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>. <b>ISyncMgrScheduleWizardUIOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrScheduleWizardUIOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrschedulewizarduioperation-initwizard">InitWizard</a>
</td>
<td align="left" width="63%">
Initializes the sync schedule wizard.

</td>
</tr>
</table> 


## -remarks



The wizard can be invoked by CoCreating CLSID_SyncMgrScheduleWizard, which is typically done when Sync Center calls <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a>, specifying SYNCMGR_OBJECTID_ShowSchedule for the object ID.
      



