---
UID: NN:syncmgr.ISyncMgrScheduleWizardUIOperation
title: ISyncMgrScheduleWizardUIOperation
author: windows-driver-content
description: Exposes a method that allows a handler to display the sync schedule wizard for the handler.
old-location: shell\ISyncMgrScheduleWizardUIOperation.htm
old-project: shell
ms.assetid: dcbe22fb-624f-4784-b1c3-5c463d6502a3
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ISyncMgrScheduleWizardUIOperation, ISyncMgrScheduleWizardUIOperation interface [Windows Shell], ISyncMgrScheduleWizardUIOperation interface [Windows Shell],described, _shell_ISyncMgrScheduleWizardUIOperation, shell.ISyncMgrScheduleWizardUIOperation, syncmgr/ISyncMgrScheduleWizardUIOperation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrScheduleWizardUIOperation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrScheduleWizardUIOperation interface


## -description


Exposes a method that allows a handler to display the sync schedule wizard for the handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrScheduleWizardUIOperation</b> interface inherits from <a href="https://msdn.microsoft.com/6fa4b0ac-3c75-4cda-b20d-582a3e18fb28">ISyncMgrUIOperation</a>. <b>ISyncMgrScheduleWizardUIOperation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f88a9a13-6e07-400a-bb05-75b1267343a9">InitWizard</a>
</td>
<td align="left" width="63%">
Initializes the sync schedule wizard.

</td>
</tr>
</table> 


## -remarks




        The wizard can be invoked by CoCreating CLSID_SyncMgrScheduleWizard, which is typically done when Sync Center calls <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a>, specifying SYNCMGR_OBJECTID_ShowSchedule for the object ID.
      



