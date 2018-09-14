---
UID: NF:bitscfg.IBITSExtensionSetup.GetCleanupTask
title: IBITSExtensionSetup::GetCleanupTask
author: windows-sdk-content
description: Use the GetCleanupTask method to retrieve an interface pointer to the cleanup task associated with the virtual directory.
old-location: bits\ibitsextensionsetup_getcleanuptask.htm
tech.root: Bits
ms.assetid: ffa89d5b-7ba1-433b-a93d-032012906258
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetCleanupTask, GetCleanupTask method [BITS], GetCleanupTask method [BITS],IBITSExtensionSetup interface, IBITSExtensionSetup interface [BITS],GetCleanupTask method, IBITSExtensionSetup.GetCleanupTask, IBITSExtensionSetup::GetCleanupTask, _drz_ibitsextensionsetup_getcleanuptask, bits.ibitsextensionsetup_getcleanuptask, bitscfg/IBITSExtensionSetup::GetCleanupTask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsMgr.dll
api_name:
 - IBITSExtensionSetup.GetCleanupTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on Windows XP
---

# IBITSExtensionSetup::GetCleanupTask


## -description


Use the 
<b>GetCleanupTask</b> method to retrieve an interface pointer to the cleanup task associated with the virtual directory.


## -parameters




### -param riid [in]

Identifies the task scheduler interface to return in <i>ppTask</i>. For a list of identifiers, see the 
<a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a> method.


### -param ppUnk

TBD




#### - ppTask [out]

A pointer to the interface specified by <i>riid</i>. Use the interface to modify the properties of the task. Release <i>ppTask</i> when done.


## -returns



This method returns <b>S_OK</b> for success. Otherwise, the method returns <b>S_FALSE</b> if a task has not been created for the virtual directory.




## -remarks



When you create a virtual directory and 
<a href="https://msdn.microsoft.com/5b68dea2-f9a7-4a99-93d3-62c4f24b769f">enable</a> it for BITS uploads, BITS adds a work item in the 
<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>. The work item cleans up the virtual directory once every 12 hours by deleting jobs that have not been modified within the time-out period. To specify the time-out period, set the 
<a href="https://msdn.microsoft.com/08a40cc1-ec6d-4b65-971a-15c7b06df148">BITSSessionTimeout</a> IIS extension property.

To change the cleanup schedule, see the <a href="https://msdn.microsoft.com/08a40cc1-ec6d-4b65-971a-15c7b06df148">BITSCleanupUseDefault</a> BITS IIS extension property.




## -see-also




<a href="https://msdn.microsoft.com/5b68dea2-f9a7-4a99-93d3-62c4f24b769f">IBITSExtensionSetup::EnableBITSUploads</a>



<a href="https://msdn.microsoft.com/edca833f-16ec-40c7-a3d8-f893a635b8e2">IBITSExtensionSetup::GetCleanupTaskName</a>
 

 

