---
UID: NF:timeprov.TimeProvOpen
title: TimeProvOpen function (timeprov.h)
description: A callback function that is called by the time provider manager when the time provider DLL is loaded.
helpviewer_keywords: ["TimeProvOpen","TimeProvOpen callback","TimeProvOpen callback function","_win32_timeprovopen","base.timeprovopen","timeprov/TimeProvOpen"]
old-location: base\timeprovopen.htm
tech.root: winprog
ms.assetid: cf4f8d00-4c6f-4036-a179-444ff7505ab4
ms.date: 12/05/2018
ms.keywords: TimeProvOpen, TimeProvOpen callback, TimeProvOpen callback function, _win32_timeprovopen, base.timeprovopen, timeprov/TimeProvOpen
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TimeProvOpen
 - timeprov/TimeProvOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Timeprov.h
api_name:
 - TimeProvOpen
---

# TimeProvOpen function


## -description

A callback function that is called by the time provider manager when the time provider DLL is loaded.

## -parameters

### -param wszName [in]

The provider name.

### -param pSysCallbacks [in]

A pointer to a 
<a href="/windows/desktop/api/timeprov/ns-timeprov-timeprovsyscallbacks">TimeProvSysCallbacks</a> structure that specifies pointers to the functions provided by the time service to the time provider. The system allocates this structure, and it is destroyed when the function returns. Therefore, you must copy the information to another buffer.

### -param phTimeProv [out]

A pointer to a buffer that contains a handle to the provider. The time provider manager uses this handle to communicate with the time provider.

## -returns

If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.

## -remarks

You should return from this callback function as quickly as possible. Perform any initialization in another thread.


#### Examples

For an example, see <a href="/windows/desktop/SysInfo/sample-time-provider">Sample Time Provider</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/timeprov/nc-timeprov-alertsamplesavailfunc">AlertSamplesAvailFunc</a>



<a href="/windows/desktop/api/timeprov/nc-timeprov-gettimesysinfofunc">GetTimeSysInfoFunc</a>



<a href="/windows/desktop/api/timeprov/nc-timeprov-logtimeproveventfunc">LogTimeProvEventFunc</a>



<a href="/windows/desktop/api/timeprov/nc-timeprov-setproviderstatusfunc">SetProviderStatusFunc</a>



<a href="/windows/desktop/api/timeprov/ns-timeprov-timeprovsyscallbacks">TimeProvSysCallbacks</a>