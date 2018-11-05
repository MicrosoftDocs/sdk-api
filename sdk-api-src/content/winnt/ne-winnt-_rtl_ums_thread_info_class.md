---
UID: NE:winnt._RTL_UMS_THREAD_INFO_CLASS
title: "_RTL_UMS_THREAD_INFO_CLASS"
author: windows-sdk-content
description: Represents classes of information about user-mode scheduling (UMS) threads.
old-location: base\ums_thread_info_class.htm
tech.root: procthread
ms.assetid: 2d6730b2-4d01-45f5-9514-0d91806f50d5
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PRTL_UMS_THREAD_INFO_CLASS, PUMS_THREAD_INFO_CLASS, PUMS_THREAD_INFO_CLASS enumeration pointer, RTL_UMS_THREAD_INFO_CLASS, UMS_THREAD_INFO_CLASS, UMS_THREAD_INFO_CLASS enumeration, UmsThreadAffinity, UmsThreadInvalidInfoClass, UmsThreadIsSuspended, UmsThreadIsTerminated, UmsThreadMaxInfoClass, UmsThreadPriority, UmsThreadTeb, UmsThreadUserContext, _RTL_UMS_THREAD_INFO_CLASS, base.ums_thread_info_class, winbase/PUMS_THREAD_INFO_CLASS, winbase/UMS_THREAD_INFO_CLASS, winbase/UmsThreadAffinity, winbase/UmsThreadInvalidInfoClass, winbase/UmsThreadIsSuspended, winbase/UmsThreadIsTerminated, winbase/UmsThreadMaxInfoClass, winbase/UmsThreadPriority, winbase/UmsThreadTeb, winbase/UmsThreadUserContext, winnt/PUMS_THREAD_INFO_CLASS, winnt/UMS_THREAD_INFO_CLASS, winnt/UmsThreadAffinity, winnt/UmsThreadInvalidInfoClass, winnt/UmsThreadIsSuspended, winnt/UmsThreadIsTerminated, winnt/UmsThreadMaxInfoClass, winnt/UmsThreadPriority, winnt/UmsThreadTeb, winnt/UmsThreadUserContext"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
 - WinNT.h
api_name:
 - UMS_THREAD_INFO_CLASS
product: Windows
targetos: Windows
req.typenames: RTL_UMS_THREAD_INFO_CLASS, *PRTL_UMS_THREAD_INFO_CLASS
req.redist: 
---

# _RTL_UMS_THREAD_INFO_CLASS enumeration


## -description


Represents classes of information about user-mode scheduling (UMS) threads.

This enumeration is used by the <a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a> and <a href="https://msdn.microsoft.com/19f190fd-1f78-4bb6-93eb-73a5c522b44d">SetUmsThreadInformation</a> functions.


## -enum-fields




### -field UmsThreadInvalidInfoClass

Reserved.


### -field UmsThreadUserContext

Application-defined information stored in a UMS thread context.


### -field UmsThreadPriority

Reserved.


### -field UmsThreadAffinity

Reserved.


### -field UmsThreadTeb

The thread execution block (<a href="https://msdn.microsoft.com/fc77fc09-6319-4daa-ac96-1ded661ef800">TEB</a>) for a UMS thread. This information class can only be queried; it cannot be set.


### -field UmsThreadIsSuspended

The suspension status of the thread. This information can only be queried; it cannot be set.


### -field UmsThreadIsTerminated

The termination status of the thread. This information can only be queried; it cannot be set.


### -field UmsThreadMaxInfoClass

Reserved.

