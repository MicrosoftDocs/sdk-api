---
UID: NF:syncmgr.ISyncMgrScheduleWizardUIOperation.InitWizard
title: ISyncMgrScheduleWizardUIOperation::InitWizard method
author: windows-driver-content
description: Initializes the sync schedule wizard.
old-location: shell\ISyncMgrScheduleWizardUIOperation_InitWizard.htm
old-project: shell
ms.assetid: f88a9a13-6e07-400a-bb05-75b1267343a9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ISyncMgrScheduleWizardUIOperation, ISyncMgrScheduleWizardUIOperation interface [Windows Shell], InitWizard method, ISyncMgrScheduleWizardUIOperation::InitWizard, InitWizard method [Windows Shell], InitWizard method [Windows Shell], ISyncMgrScheduleWizardUIOperation interface, InitWizard,ISyncMgrScheduleWizardUIOperation.InitWizard, _shell_ISyncMgrScheduleWizardUIOperation_InitWizard, shell.ISyncMgrScheduleWizardUIOperation_InitWizard, syncmgr/ISyncMgrScheduleWizardUIOperation::InitWizard
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	ISyncMgrScheduleWizardUIOperation.InitWizard
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrScheduleWizardUIOperation::InitWizard method


## -description


Initializes the sync schedule wizard.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a handler ID as a Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



