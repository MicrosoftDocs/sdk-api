---
UID: NF:mmc.IConsolePower.ResetIdleTimer
title: IConsolePower::ResetIdleTimer (mmc.h)
description: The ResetIdleTimer method resets the specified power management idle timers.
helpviewer_keywords: ["ES_DISPLAY_REQUIRED","ES_SYSTEM_REQUIRED","IConsolePower interface [MMC]","ResetIdleTimer method","IConsolePower.ResetIdleTimer","IConsolePower::ResetIdleTimer","ResetIdleTimer","ResetIdleTimer method [MMC]","ResetIdleTimer method [MMC]","IConsolePower interface","_slate_iconsolepower_resetidletimer","mmc.iconsolepower_resetidletimer","mmc/IConsolePower::ResetIdleTimer"]
old-location: mmc\iconsolepower_resetidletimer.htm
tech.root: mmc
ms.assetid: 83de4b7f-3214-4354-a4a0-721054e2e899
ms.date: 12/05/2018
ms.keywords: ES_DISPLAY_REQUIRED, ES_SYSTEM_REQUIRED, IConsolePower interface [MMC],ResetIdleTimer method, IConsolePower.ResetIdleTimer, IConsolePower::ResetIdleTimer, ResetIdleTimer, ResetIdleTimer method [MMC], ResetIdleTimer method [MMC],IConsolePower interface, _slate_iconsolepower_resetidletimer, mmc.iconsolepower_resetidletimer, mmc/IConsolePower::ResetIdleTimer
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConsolePower::ResetIdleTimer
 - mmc/IConsolePower::ResetIdleTimer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsolePower.ResetIdleTimer
---

# IConsolePower::ResetIdleTimer


## -description

The 
ResetIdleTimer method resets the specified power management idle timers.

## -parameters

### -param dwFlags [in]

The flags used to reset idle timers. One or more of the following flags can be used. For more information, see 
<a href="/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate">SetThreadExecutionState</a>.



#### ES_DISPLAY_REQUIRED

Resets the display (monitor) idle timer.



#### ES_SYSTEM_REQUIRED

Resets the system idle timer.

## -returns

If successful, the return value is S_OK. This method will return S_FALSE when invoked on a system that does not support power management. Other return values indicate an error code.

## -remarks

Call <b>IConsolePower::ResetIdleTimer</b> instead of calling 
<a href="/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate">SetThreadExecutionState</a>. Snap-ins must not call the <b>SetThreadExecutionState</b> function directly, doing so causes conflicts if multiple snap-ins are running on the same thread. Instead, snap-ins should call 
SetExecutionState. Resetting an idle timer causes it to start over in tracking the idle period. If a snap-in does not specify a continuous execution state by calling <a href="/windows/desktop/api/mmc/nf-mmc-iconsolepower-setexecutionstate">IConsolePower::SetExecutionState</a>, it can periodically call 
ResetIdleTimer to prolong the time before the system or display power-management routines are invoked.


#### Examples


```cpp
HRESULT hr;

// Reset both the display and system idle timers.
// pConsolePower was created previously by
// the CoCreateInstance method.
hr = pConsolePower->ResetIdleTimer(
             ES_DISPLAY_REQUIRED | ES_SYSTEM_REQUIRED);
switch (hr)
{
    case S_OK:
        OutputDebugString(_T("ResetIdleTimer: Succeeded\n"));
        break;

    case S_FALSE:
        // The system does not support power management.
        OutputDebugString(_T("ResetIdleTimer: Unsupported\n"));
        break;

    default:
        // Unexpected error occurred.
        OutputDebugString(_T("ResetIdleTimer: Failure\n"));
        break;
}
```

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-iconsolepower-setexecutionstate">IConsolePower::SetExecutionState</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate">SetThreadExecutionState</a>