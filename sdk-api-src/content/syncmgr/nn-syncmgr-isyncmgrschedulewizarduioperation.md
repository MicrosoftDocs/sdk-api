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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrScheduleWizardUIOperation
 - syncmgr/ISyncMgrScheduleWizardUIOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrScheduleWizardUIOperation
---

# ISyncMgrScheduleWizardUIOperation interface


## -description

Exposes a method that allows a handler to display the sync schedule wizard for the handler.

## -inheritance

The <b>ISyncMgrScheduleWizardUIOperation</b> interface inherits from <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a>. <b>ISyncMgrScheduleWizardUIOperation</b> also has these types of members:

## -remarks

The wizard can be invoked by CoCreating CLSID_SyncMgrScheduleWizard, which is typically done when Sync Center calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">ISyncMgrHandler::GetObject</a>, specifying SYNCMGR_OBJECTID_ShowSchedule for the object ID.
