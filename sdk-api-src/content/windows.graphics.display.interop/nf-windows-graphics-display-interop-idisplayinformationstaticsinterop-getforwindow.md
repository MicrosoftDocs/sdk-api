---
UID: NF:windows.graphics.display.interop.IDisplayInformationStaticsInterop.GetForWindow
title: IDisplayInformationStaticsInterop::GetForWindow
description: Retrieves a [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) object for the specified window.
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
 - IDisplayInformationStaticsInterop::GetForWindow
f1_keywords:
 - IDisplayInformationStaticsInterop::GetForWindow
 - windows.graphics.display.interop/IDisplayInformationStaticsInterop::GetForWindow
dev_langs:
 - c++
helpviewer_keywords:
 - GetForWindow
prerelease: false
---

## -description

Retrieves a [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) object for the specified window. **GetForWindow** always allocates and returns a new **DisplayInformation**.

## -parameters

### -param window

Type: \[in\] **[HWND](/windows/win32/winprog/windows-data-types)**

The window's handle.

### -param riid

Type: \[in\] **[REFIID](/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)**

The **GUID** of the [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) class.

### -param displayInfo

Type: \[iid_is\]\[retval\]\[out\] **[void](/windows/win32/winprog/windows-data-types)\*\***

A pointer to a memory block that receives a pointer to the returned [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

So that [DisplayInformation](/uwp/api/windows.graphics.display.displayinformation) can process window movements and DPI change messages, it hooks the message loop of your **HWND**. In order to ensure that that happens smoothly, **GetForWindow** has the following requirements:

* The argument of *window* must be the **HWND** of a top-level window that's owned by the current thread.
* The current thread must have a [Windows.System.DispatcherQueue](/uwp/api/windows.system.dispatcherqueue) running, in order to receive events.
* The current thread can be MTA or STA.

You're responsible for: caching the created **DisplayInformation** for as long as the argument of *window* is relevant; de-registering event handlers; and dropping the last reference in order to destroy the **DisplayInformation** instance.

## Examples

It's vital for an app that renders wide-color gamut and high-dynamic range content to adjust dynamically to changing conditions of the monitor; or when moving between monitors. On a laptop, the user might adjust the brightness of the screen, and that can adjust the tone-mapping parameters provided to apps.

```cppwinrt
// It's safe, and recommended, to cache the DisplayInformation created from an HWND,
// since it safely provides the latest information and event handlers for when
// changes take place.

#include <Windows.Graphics.Display.Interop.h>
#include <winrt/Windows.Graphics.Display.h>
using namespace winrt::Windows::Graphics::Display;
...
void ReadHdrParametersFromDisplayInformation(HWND myWindow)
{
    auto factory{ winrt::get_activation_factory<DisplayInformation,
        IDisplayInformationStaticsInterop>() };

    DisplayInformation displayInfo{ nullptr };

    winrt::check_hresult(
        factory->GetForWindow(
            myWindow,
            winrt::guid_of<DisplayInformation>(),
            winrt::put_abi(displayInfo)
        )
    );

    auto colorInfo{ displayInfo.GetAdvancedColorInfo() };
    // Here you can read colorInfo properties such as:
    // * CurrentAdvancedColorKind
    // * RedPrimary, BluePrimary, GreenPrimary, WhitePoint
    // * MinLuminanceInNits, MaxLuminanceInNits
    // * MaxAverageFullFrameLuminanceInNits, SdrWhiteLevelInNits
    // ... and adapt your rendering.

    // You can also subscribe event handlers to listen for changes:
    displayInfo.AdvancedColorInfoChanged(
        [&](auto sender, auto args)
        {
            // Handle the event.
        }
    );

    // Cache the DisplayInformation object for as long as your window
    // is alive: it always provides fresh data for your window.
}
```

## -see-also
