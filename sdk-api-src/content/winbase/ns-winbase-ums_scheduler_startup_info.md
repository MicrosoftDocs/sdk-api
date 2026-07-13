---
UID: NS:winbase._UMS_SCHEDULER_STARTUP_INFO
title: UMS_SCHEDULER_STARTUP_INFO (winbase.h)
description: Specifies attributes for a user-mode scheduling (UMS) scheduler thread.
helpviewer_keywords: ["*PUMS_SCHEDULER_STARTUP_INFO","PUMS_SCHEDULER_STARTUP_INFO","PUMS_SCHEDULER_STARTUP_INFO structure pointer","UMS_SCHEDULER_STARTUP_INFO","UMS_SCHEDULER_STARTUP_INFO structure","_UMS_SCHEDULER_STARTUP_INFO","base.ums_scheduler_startup_info","winbase/PUMS_SCHEDULER_STARTUP_INFO","winbase/UMS_SCHEDULER_STARTUP_INFO"]
old-location: base\ums_scheduler_startup_info.htm
tech.root: backup
ms.assetid: e3f7b1b7-d2b8-432d-bce7-3633292e855b
ms.date: 12/05/2018
ms.keywords: '*PUMS_SCHEDULER_STARTUP_INFO, PUMS_SCHEDULER_STARTUP_INFO, PUMS_SCHEDULER_STARTUP_INFO structure pointer, UMS_SCHEDULER_STARTUP_INFO, UMS_SCHEDULER_STARTUP_INFO structure, _UMS_SCHEDULER_STARTUP_INFO, base.ums_scheduler_startup_info, winbase/PUMS_SCHEDULER_STARTUP_INFO, winbase/UMS_SCHEDULER_STARTUP_INFO'
req.header: winbase.h
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
targetos: Windows
req.typenames: UMS_SCHEDULER_STARTUP_INFO, *PUMS_SCHEDULER_STARTUP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _UMS_SCHEDULER_STARTUP_INFO
 - winbase/_UMS_SCHEDULER_STARTUP_INFO
 - PUMS_SCHEDULER_STARTUP_INFO
 - winbase/PUMS_SCHEDULER_STARTUP_INFO
 - UMS_SCHEDULER_STARTUP_INFO
 - winbase/UMS_SCHEDULER_STARTUP_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - UMS_SCHEDULER_STARTUP_INFO
---

# UMS_SCHEDULER_STARTUP_INFO structure


## -description

Specifies attributes for a user-mode scheduling (UMS) scheduler thread. The <a href="/windows/desktop/api/winbase/nf-winbase-enterumsschedulingmode">EnterUmsSchedulingMode</a> function uses this structure.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -struct-fields

### -field UmsVersion

The UMS version for which the application was built. This parameter must be <b>UMS_VERSION</b>.

### -field CompletionList

A pointer to a UMS completion list to associate with the calling thread.

### -field SchedulerProc

A pointer to an application-defined <a href="/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a> entry point function. The system calls this function when the calling thread has been converted to UMS and is ready to run UMS worker threads. Subsequently, it calls this function when a UMS worker thread running on the calling thread yields or blocks.

### -field SchedulerParam

An application-defined parameter to pass to the specified <a href="/windows/desktop/api/winnt/nc-winnt-rtl_ums_scheduler_entry_point">UmsSchedulerProc</a> function.