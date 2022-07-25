---
UID: NF:windows.graphics.display.interop.IDisplayInformationStaticsInterop.GetForMonitor
title: IDisplayInformationStaticsInterop::GetForMonitor
description: Retrieves a [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) object for the specified monitor.
tech.root: winrt
ms.date: 05/17/2022
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: windows.graphics.display.interop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - windows.graphics.display.interop.h
api_name:
 - IDisplayInformationStaticsInterop::GetForMonitor
f1_keywords:
 - IDisplayInformationStaticsInterop::GetForMonitor
 - windows.graphics.display.interop/IDisplayInformationStaticsInterop::GetForMonitor
dev_langs:
 - c++
helpviewer_keywords:
 - GetForMonitor
prerelease: false
---

## -description

Retrieves a [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) object for the specified monitor. **GetForMonitor** always allocates and returns a new **DisplayInformation**.

## -parameters

### -param monitor

Type: \[in]\ **[HMONITOR](/windows/win32/winprog/windows-data-types)**

The monitor's handle.

### -param riid

Type: \[in]\ **[REFIID](/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)**

The **GUID** of the [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) class.

### -param displayInfo

Type: \[iid_is\]\[retval\]\[out\] **[void](/windows/win32/winprog/windows-data-types)\*\***

A pointer to a memory block that receives a pointer to the returned [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

Considerations:

* Window movements are not tracked, since there is no window.
* Any scale factor returned by the [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) is the current scale factor for the entire monitor. DPI virtualization acts in the same way as for [GetScaleFactorForMonitor](/windows/win32/api/shellscalingapi/nf-shellscalingapi-getscalefactorformonitor), which is the underlying API used to read scale in this case.
* If you wish to register for events, then the current thread must have a [Windows.System.DispatcherQueue](/uwp/api/windows.system.dispatcherqueue) running, in order to receive events. That **DispatcherQueue** will be snapped upon the call to **GetForMonitor**. If there is no **DispatcherQueue**, then an exception (at the application binary interface level, a **HRESULT**) is returned in the event handler registration methods.
* The current thread can be MTA or STA.

You're responsible for: caching the created **DisplayInformation** for as long as the argument of *monitor* is relevant; de-registering event handlers; and dropping the last reference in order to destroy the **DisplayInformation** instance.

## Examples

See the code example in [IDisplayInformationStaticsInterop::GetForWindow](nf-windows-graphics-display-interop-idisplayinformationstaticsinterop-getforwindow.md).

## -see-also
