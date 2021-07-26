---
UID: NN:windows.ui.xaml.hosting.desktopwindowxamlsource.IDesktopWindowXamlSourceNative2
tech.root: winrt
title: IDesktopWindowXamlSourceNative2
ms.date: 07/25/2021
targetos: Windows
description: Provides a method that enables the WinRT XAML framework to process Windows messages for a **DesktopWindowXamlSource** object that hosts a WinRT XAML control.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: windows.ui.xaml.hosting.desktopwindowxamlsource.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1903 (build 18362) 
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
 - windows.ui.xaml.hosting.desktopwindowxamlsource.h
api_name:
 - IDesktopWindowXamlSourceNative2
f1_keywords:
 - IDesktopWindowXamlSourceNative2
 - windows.ui.xaml.hosting.desktopwindowxamlsource/IDesktopWindowXamlSourceNative2
dev_langs:
 - c++
---

## -description

Provides a method that enables the WinRT XAML framework to process Windows messages for a [DesktopWindowXamlSource](/uwp/api/windows.ui.xaml.hosting.desktopwindowxamlsource) object that hosts a WinRT XAML control.

## -remarks

This interface is implemented by the [DesktopWindowXamlSource](/uwp/api/windows.ui.xaml.hosting.desktopwindowxamlsource) class. **DesktopWindowXamlSource** is a key component the [WinRT XAML hosting API](/windows/apps/desktop/modernize/using-the-xaml-hosting-api), which desktop apps can use to host WinRT XAML controls in any UI element that is associated with a window handle (this feature is also called *XAML Islands*).

## -see-also

[Using the UWP XAML hosting API in a C++ desktop (Win32) app](/windows/apps/desktop/modernize/using-the-xaml-hosting-api)