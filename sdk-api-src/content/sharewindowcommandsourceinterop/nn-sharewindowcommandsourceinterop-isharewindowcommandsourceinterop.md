---
UID: NN:sharewindowcommandsourceinterop.IShareWindowCommandSourceInterop
title: IShareWindowCommandSourceInterop
description: A native interoperation interface that allows getting a [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource) object.
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
 - IShareWindowCommandSourceInterop
f1_keywords:
 - IShareWindowCommandSourceInterop
 - sharewindowcommandsourceinterop/IShareWindowCommandSourceInterop
---

## -description

A native interoperation interface that allows getting a [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource) object. This interface is available in C++ only. Also see [IShareWindowCommandSourceInterop.GetForWindow](nf-sharewindowcommandsourceinterop-isharewindowcommandsourceinterop-getforwindow.md).

> [!NOTE]
> Thank you for your interest in consuming the **ShareWindowCommandSource** API within your real-time communication application.
>
> The **ShareWindowCommandSource** API is a limited access feature.
>
> Please contact [onairapi@microsoft.com](mailto://onairapi@microsoft.com) for more information, and to request an unlock token.

## -remarks

Here's a code example.

```cppwinrt
auto interop_factory = winrt::get_activation_factory
    <winrt::Windows::UI::Shell::ShareWindowCommandSource,
    IShareWindowCommandSourceInterop>();
        
winrt::check_hresult(interop_factory->GetForWindow(
    m_hwndOfMyAppCallWindow,
    winrt::guid_of<winrt::Windows::UI::Shell::IShareWindowCommandSource>(), 
    winrt::put_abi(m_shareWindowCommandSource)));
```

## -see-also

* [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource)

* [IShareWindowCommandSourceInterop.GetForWindow](nf-sharewindowcommandsourceinterop-isharewindowcommandsourceinterop-getforwindow.md)
