---
UID: NF:bitscfg.IBITSExtensionSetup.GetCleanupTask
title: IBITSExtensionSetup::GetCleanupTask (bitscfg.h)
description: Use the GetCleanupTask method to retrieve an interface pointer to the cleanup task associated with the virtual directory.
helpviewer_keywords: ["GetCleanupTask","GetCleanupTask method [BITS]","GetCleanupTask method [BITS]","IBITSExtensionSetup interface","IBITSExtensionSetup interface [BITS]","GetCleanupTask method","IBITSExtensionSetup.GetCleanupTask","IBITSExtensionSetup::GetCleanupTask","_drz_ibitsextensionsetup_getcleanuptask","bits.ibitsextensionsetup_getcleanuptask","bitscfg/IBITSExtensionSetup::GetCleanupTask"]
old-location: bits\ibitsextensionsetup_getcleanuptask.htm
tech.root: Bits
ms.assetid: ffa89d5b-7ba1-433b-a93d-032012906258
ms.date: 12/05/2018
ms.keywords: GetCleanupTask, GetCleanupTask method [BITS], GetCleanupTask method [BITS],IBITSExtensionSetup interface, IBITSExtensionSetup interface [BITS],GetCleanupTask method, IBITSExtensionSetup.GetCleanupTask, IBITSExtensionSetup::GetCleanupTask, _drz_ibitsextensionsetup_getcleanuptask, bits.ibitsextensionsetup_getcleanuptask, bitscfg/IBITSExtensionSetup::GetCleanupTask
req.header: bitscfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bitscfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: BitsMgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on Windows XP
ms.custom: 19H1
f1_keywords:
 - IBITSExtensionSetup::GetCleanupTask
 - bitscfg/IBITSExtensionSetup::GetCleanupTask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsMgr.dll
api_name:
 - IBITSExtensionSetup.GetCleanupTask
---

# IBITSExtensionSetup::GetCleanupTask


## -description

Use the 
<b>GetCleanupTask</b> method to retrieve an interface pointer to the cleanup task associated with the virtual directory.

## -parameters

### -param riid [in]

Identifies the task scheduler interface to return in <i>ppTask</i>. For a list of identifiers, see the 
<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">ITaskScheduler::Activate</a> method.

### -param ppUnk [out]

A pointer to the interface specified by <i>riid</i>. Use the interface to modify the properties of the task. Release <i>ppTask</i> when done.

## -returns

This method returns <b>S_OK</b> for success. Otherwise, the method returns <b>S_FALSE</b> if a task has not been created for the virtual directory.

## -remarks

When you create a virtual directory and 
<a href="/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads">enable</a> it for BITS uploads, BITS adds a work item in the 
<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>. The work item cleans up the virtual directory once every 12 hours by deleting jobs that have not been modified within the time-out period. To specify the time-out period, set the 
<a href="/windows/desktop/Bits/bits-iis-extension-properties">BITSSessionTimeout</a> IIS extension property.

To change the cleanup schedule, see the <a href="/windows/desktop/Bits/bits-iis-extension-properties">BITSCleanupUseDefault</a> BITS IIS extension property.

## -see-also

<a href="/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads">IBITSExtensionSetup::EnableBITSUploads</a>



<a href="/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptaskname">IBITSExtensionSetup::GetCleanupTaskName</a>