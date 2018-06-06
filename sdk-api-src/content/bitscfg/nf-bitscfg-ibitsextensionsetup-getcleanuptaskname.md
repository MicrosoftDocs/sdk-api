---
UID: NF:bitscfg.IBITSExtensionSetup.GetCleanupTaskName
title: IBITSExtensionSetup::GetCleanupTaskName
author: windows-sdk-content
description: Use the GetCleanupTaskName method to retrieve the name of the cleanup task associated with the virtual directory.
old-location: bits\ibitsextensionsetup_getcleanuptaskname.htm
old-project: Bits
ms.assetid: edca833f-16ec-40c7-a3d8-f893a635b8e2
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetCleanupTaskName, GetCleanupTaskName method [BITS], GetCleanupTaskName method [BITS],IBITSExtensionSetup interface, IBITSExtensionSetup interface [BITS],GetCleanupTaskName method, IBITSExtensionSetup.GetCleanupTaskName, IBITSExtensionSetup::GetCleanupTaskName, _drz_ibitsextensionsetup_getcleanuptaskname, bits.ibitsextensionsetup_getcleanuptaskname, bitscfg/IBITSExtensionSetup::GetCleanupTaskName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BITS_FILE_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsMgr.dll
api_name:
 - IBITSExtensionSetup.GetCleanupTaskName
product: Windows
targetos: Windows
req.lib: 
req.dll: BitsMgr.dll
req.irql: 
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451004">enable</a> it for BITS uploads, BITS adds a work item in the 
<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>. The work item cleans up the virtual directory once every 12 hours by deleting jobs that have not been modified within the time-out period. To specify the time-out period, set the 
<a href="https://msdn.microsoft.com/08a40cc1-ec6d-4b65-971a-15c7b06df148">BITSSessionTimeout</a> IIS extension property.

Use the <i>pTaskName</i> name as an input parameter to the Schtasks.exe executable file, which you can use to change the properties of the cleanup task from a script.




## -see-also




<a href="https://msdn.microsoft.com/5b68dea2-f9a7-4a99-93d3-62c4f24b769f">IBITSExtensionSetup::EnableBITSUploads</a>



<a href="https://msdn.microsoft.com/ffa89d5b-7ba1-433b-a93d-032012906258">IBITSExtensionSetup::GetCleanupTask</a>
 

 

