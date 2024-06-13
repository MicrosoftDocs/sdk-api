---
UID: NN:sharewindowcommandsourceinterop.IShareWindowCommandEventArgsInterop
title: IShareWindowCommandEventArgsInterop
description: Gets the [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource) object corresponding to a window identifier (a window handle). (IShareWindowCommandEventArgsInterop)
tech.root: winrt
prerelease: false
ms.date: 06/09/2021
targetos: Windows
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: sharewindowcommandsourceinterop.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.unicode-ansi: 
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - sharewindowcommandsourceinterop.h
api_name:
 - IShareWindowCommandEventArgsInterop
f1_keywords:
 - IShareWindowCommandEventArgsInterop
 - sharewindowcommandsourceinterop/IShareWindowCommandEventArgsInterop
---

## -description

A native interoperation interface that allows getting a window identifier (a window handle) from a Windows Runtime [Windows::UI::Shell::ShareWindowCommandEventArgs](/uwp/api/windows.ui.shell.sharewindowcommandeventargs) object. This interface is available in C++ only.

> [!IMPORTANT]
> The **IShareWindowCommandEventArgsInterop** API is part of a Limited Access Feature (see [LimitedAccessFeatures class](/uwp/api/windows.applicationmodel.limitedaccessfeatures)). For more information or to request an unlock token, contact [Microsoft Support](https://aka.ms/LAFAccessRequests).

## -remarks

You can query interface a [ShareWindowCommandEventArgs](/uwp/api/windows.ui.shell.sharewindowcommandeventargs) object for **IShareWindowCommandEventArgsInterop**.

```cpp
void MyAppShareController::OnCommandInvoked(
    winrt::Windows::UI::Shell::ShareWindowCommandSource const& /*sender*/,
    winrt::Windows::UI::Shell::ShareWindowCommandEventArgs const& args)
{
    auto eventArgsInterop = eventArgs.as<IShareWindowCommandEventArgsInterop>();
    HWND windowId = 0;
    winrt::check_hresult(eventArgsInterop->get_WindowId(&windowId));

    ...
}
```

## -see-also

* [ShareWindowCommandEventArgs](/uwp/api/windows.ui.shell.sharewindowcommandeventargs)
