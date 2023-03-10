---
UID: NF:bitscfg.IBITSExtensionSetup.GetCleanupTaskName
title: IBITSExtensionSetup::GetCleanupTaskName (bitscfg.h)
description: Use the GetCleanupTaskName method to retrieve the name of the cleanup task associated with the virtual directory.
helpviewer_keywords: ["GetCleanupTaskName","GetCleanupTaskName method [BITS]","GetCleanupTaskName method [BITS]","IBITSExtensionSetup interface","IBITSExtensionSetup interface [BITS]","GetCleanupTaskName method","IBITSExtensionSetup.GetCleanupTaskName","IBITSExtensionSetup::GetCleanupTaskName","_drz_ibitsextensionsetup_getcleanuptaskname","bits.ibitsextensionsetup_getcleanuptaskname","bitscfg/IBITSExtensionSetup::GetCleanupTaskName"]
old-location: bits\ibitsextensionsetup_getcleanuptaskname.htm
tech.root: Bits
ms.assetid: edca833f-16ec-40c7-a3d8-f893a635b8e2
ms.date: 12/05/2018
ms.keywords: GetCleanupTaskName, GetCleanupTaskName method [BITS], GetCleanupTaskName method [BITS],IBITSExtensionSetup interface, IBITSExtensionSetup interface [BITS],GetCleanupTaskName method, IBITSExtensionSetup.GetCleanupTaskName, IBITSExtensionSetup::GetCleanupTaskName, _drz_ibitsextensionsetup_getcleanuptaskname, bits.ibitsextensionsetup_getcleanuptaskname, bitscfg/IBITSExtensionSetup::GetCleanupTaskName
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
 - IBITSExtensionSetup::GetCleanupTaskName
 - bitscfg/IBITSExtensionSetup::GetCleanupTaskName
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
 - IBITSExtensionSetup.GetCleanupTaskName
---

# IBITSExtensionSetup::GetCleanupTaskName


## -description

Use the 
<b>GetCleanupTaskName</b> method to retrieve the name of the cleanup task associated with the virtual directory.

## -parameters

### -param pTaskName [out]

Null-terminated string containing the name of the cleanup task associated with the virtual directory. If <b>NULL</b>, BITS has not created a cleanup task for the virtual directory. When done, call the <b>SysFreeString</b> function to free <i>pTaskName</i>.

## -returns

This method returns <b>S_OK</b> for success. Otherwise, the method returns <b>S_FALSE</b> if a task name has not been specified for the virtual directory.

## -remarks

When you create a virtual directory and 
<a href="/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads">enable</a> it for BITS uploads, BITS adds a work item in the 
<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>. The work item cleans up the virtual directory once every 12 hours by deleting jobs that have not been modified within the time-out period. To specify the time-out period, set the 
<a href="/windows/desktop/Bits/bits-iis-extension-properties">BITSSessionTimeout</a> IIS extension property.

Use the <i>pTaskName</i> name as an input parameter to the Schtasks.exe executable file, which you can use to change the properties of the cleanup task from a script.

## -see-also

<a href="/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads">IBITSExtensionSetup::EnableBITSUploads</a>



<a href="/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask">IBITSExtensionSetup::GetCleanupTask</a>