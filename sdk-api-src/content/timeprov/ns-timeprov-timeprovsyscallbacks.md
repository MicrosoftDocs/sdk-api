---
UID: NS:timeprov.TimeProvSysCallbacks
title: TimeProvSysCallbacks (timeprov.h)
description: Contains pointers to functions for use by the time provider.
helpviewer_keywords: ["TimeProvSysCallbacks","TimeProvSysCallbacks structure","_win32_timeprovsyscallbacks_str","base.timeprovsyscallbacks_str","timeprov/TimeProvSysCallbacks"]
old-location: base\timeprovsyscallbacks_str.htm
tech.root: winprog
ms.assetid: a38f8b26-9450-4033-bdd7-e73726c2d609
ms.date: 12/05/2018
ms.keywords: TimeProvSysCallbacks, TimeProvSysCallbacks structure, _win32_timeprovsyscallbacks_str, base.timeprovsyscallbacks_str, timeprov/TimeProvSysCallbacks
req.header: timeprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TimeProvSysCallbacks
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TimeProvSysCallbacks
 - timeprov/TimeProvSysCallbacks
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Timeprov.h
api_name:
 - TimeProvSysCallbacks
---

# TimeProvSysCallbacks structure


## -description

Contains pointers to functions for use by the time provider.

## -struct-fields

### -field dwSize

The size of the structure, in bytes.

### -field pfnGetTimeSysInfo

A pointer to the 
<a href="/windows/desktop/api/timeprov/nc-timeprov-gettimesysinfofunc">GetTimeSysInfoFunc</a> function.

### -field pfnLogTimeProvEvent

A pointer to the 
<a href="/windows/desktop/api/timeprov/nc-timeprov-logtimeproveventfunc">LogTimeProvEventFunc</a> function.

### -field pfnAlertSamplesAvail

A pointer to the 
<a href="/windows/desktop/api/timeprov/nc-timeprov-alertsamplesavailfunc">AlertSamplesAvailFunc</a> function.

### -field pfnSetProviderStatus

A pointer to the 
<a href="/windows/desktop/api/timeprov/nc-timeprov-setproviderstatusfunc">SetProviderStatusFunc</a> function.

## -see-also

<a href="/windows/desktop/api/timeprov/nc-timeprov-alertsamplesavailfunc">AlertSamplesAvailFunc</a>



<a href="/windows/desktop/api/timeprov/nc-timeprov-gettimesysinfofunc">GetTimeSysInfoFunc</a>



<a href="/windows/desktop/api/timeprov/nc-timeprov-logtimeproveventfunc">LogTimeProvEventFunc</a>



<a href="/windows/desktop/api/timeprov/nc-timeprov-setproviderstatusfunc">SetProviderStatusFunc</a>



<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a>