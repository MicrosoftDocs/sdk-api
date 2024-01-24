---
UID: NS:winbase._UMS_SYSTEM_THREAD_INFORMATION
title: UMS_SYSTEM_THREAD_INFORMATION (winbase.h)
description: Specifies a UMS scheduler thread, UMS worker thread, or non-UMS thread. The GetUmsSystemThreadInformation function uses this structure.
helpviewer_keywords: ["*PUMS_SYSTEM_THREAD_INFORMATION","PUMS_SYSTEM_THREAD_INFORMATION","PUMS_SYSTEM_THREAD_INFORMATION structure pointer","UMS_SYSTEM_THREAD_INFORMATION","UMS_SYSTEM_THREAD_INFORMATION structure","_UMS_SYSTEM_THREAD_INFORMATION","base.ums_system_thread_information","winbase/PUMS_SYSTEM_THREAD_INFORMATION","winbase/UMS_SYSTEM_THREAD_INFORMATION"]
old-location: base\ums_system_thread_information.htm
tech.root: backup
ms.assetid: eecdc592-5046-47c3-a4c6-ecb10899db3c
ms.date: 12/05/2018
ms.keywords: '*PUMS_SYSTEM_THREAD_INFORMATION, PUMS_SYSTEM_THREAD_INFORMATION, PUMS_SYSTEM_THREAD_INFORMATION structure pointer, UMS_SYSTEM_THREAD_INFORMATION, UMS_SYSTEM_THREAD_INFORMATION structure, _UMS_SYSTEM_THREAD_INFORMATION, base.ums_system_thread_information, winbase/PUMS_SYSTEM_THREAD_INFORMATION, winbase/UMS_SYSTEM_THREAD_INFORMATION'
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1 [desktop apps only],Windows 7 (64-bit only) and Windows Server 2008 R2 (64-bit only) with KB977165  installed
req.target-min-winversvr: Windows Server 2008 R2 with SP1 [desktop apps only]
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
req.typenames: UMS_SYSTEM_THREAD_INFORMATION, *PUMS_SYSTEM_THREAD_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _UMS_SYSTEM_THREAD_INFORMATION
 - winbase/_UMS_SYSTEM_THREAD_INFORMATION
 - PUMS_SYSTEM_THREAD_INFORMATION
 - winbase/PUMS_SYSTEM_THREAD_INFORMATION
 - UMS_SYSTEM_THREAD_INFORMATION
 - winbase/UMS_SYSTEM_THREAD_INFORMATION
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
 - UMS_SYSTEM_THREAD_INFORMATION
---

# UMS_SYSTEM_THREAD_INFORMATION structure

## -description

Specifies a UMS scheduler thread, UMS worker thread, or non-UMS thread.

> [!WARNING]
> As of Windows 11, user-mode scheduling is not supported. All calls fail with the error `ERROR_NOT_SUPPORTED`.

## -struct-fields

### -field UmsVersion

The UMS version.

You must set this member to UMS_VERSION before calling the [GetUmsSystemThreadInformation](/windows/desktop/api/winbase/nf-winbase-getumssystemthreadinformation) function.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.IsUmsSchedulerThread

A bitfield that specifies that the thread is a UMS scheduler thread.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.IsUmsWorkerThread

A bitfield that specifies that the thread is a UMS worker thread.

### -field DUMMYUNIONNAME.ThreadUmsFlags

## -remarks

Used by the [GetUmsSystemThreadInformation](/windows/desktop/api/winbase/nf-winbase-getumssystemthreadinformation) function.

At most one of **IsUmsSchedulerThread** and **IsUmsWorkerThread** will be set.

If both **IsUmsSchedulerThread** and **IsUmsWorkerThread** are clear then the thread is a non-UMS thread.
