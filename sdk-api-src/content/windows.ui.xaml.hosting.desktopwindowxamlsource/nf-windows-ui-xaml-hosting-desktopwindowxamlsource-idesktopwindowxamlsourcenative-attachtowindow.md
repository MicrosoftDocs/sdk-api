---
UID: NF:windows.ui.xaml.hosting.desktopwindowxamlsource.IDesktopWindowXamlSourceNative.AttachToWindow
tech.root: winrt
title: IDesktopWindowXamlSourceNative::AttachToWindow
ms.date: 07/25/2021
targetos: Windows
description: Attaches the current **IDesktopWindowXamlSourceNative** instance to a parent UI element in your desktop app that is associated with a window handle.
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
 - IDesktopWindowXamlSourceNative::AttachToWindow
f1_keywords:
 - IDesktopWindowXamlSourceNative::AttachToWindow
 - windows.ui.xaml.hosting.desktopwindowxamlsource/IDesktopWindowXamlSourceNative::AttachToWindow
dev_langs:
 - c++
---

## -description

Attaches the current [IDesktopWindowXamlSourceNative](nn-windows-ui-xaml-hosting-desktopwindowxamlsource-idesktopwindowxamlsourcenative.md) instance to a parent UI element in your desktop app that is associated with a window handle.

## -parameters

### -param parentWnd

Type: **HWND**

The window handle of the parent UI element in which you want to host a WinRT XAML control.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an **HRESULT** error code.

## -remarks

For a code example that demonstrates how to use this method, see [XamlBridge.cpp](https://github.com/microsoft/Xaml-Islands-Samples/blob/master/Samples/Win32/SampleCppApp/XamlBridge.cpp) in the SampleCppApp sample in the XAML Island samples repo.

> [!IMPORTANT]
> Make sure that your code calls the **AttachToWindow** method only once per [DesktopWindowXamlSource](/uwp/api/windows.ui.xaml.hosting.desktopwindowxamlsource) object. Calling this method more than once for a **DesktopWindowXamlSource** object could result in a memory leak.

## -see-also

[Using the UWP XAML hosting API in a C++ desktop (Win32) app](/windows/apps/desktop/modernize/using-the-xaml-hosting-api)