---
UID: NF:windows.ui.xaml.hosting.desktopwindowxamlsource.IDesktopWindowXamlSourceNative2.PreTranslateMessage
tech.root: winrt
title: IDesktopWindowXamlSourceNative2::PreTranslateMessage
ms.date: 07/25/2021
targetos: Windows
description: Enables the WinRT XAML framework to process a Windows message for a **DesktopWindowXamlSource** object that hosts a WinRT XAML control.
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
 - IDesktopWindowXamlSourceNative2::PreTranslateMessage
f1_keywords:
 - IDesktopWindowXamlSourceNative2::PreTranslateMessage
 - windows.ui.xaml.hosting.desktopwindowxamlsource/IDesktopWindowXamlSourceNative2::PreTranslateMessage
dev_langs:
 - c++
---

## -description

Enables the WinRT XAML framework to process a Windows message for a [DesktopWindowXamlSource](/uwp/api/windows.ui.xaml.hosting.desktopwindowxamlsource) object that hosts a WinRT XAML control.

## -parameters

### -param message

Type: **const [MSG](/windows/win32/api/winuser/ns-winuser-msg)\***

The Windows message to process.

### -param result

Type: **BOOL\***

True if the message was processed; otherwise, false.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an **HRESULT** error code.

## -remarks

For a code example that demonstrates how to use this method, see [XamlBridge.cpp](https://github.com/microsoft/Xaml-Islands-Samples/blob/master/Samples/Win32/SampleCppApp/XamlBridge.cpp) in the SampleCppApp sample in the XAML Island samples repo.

## -see-also

[Using the UWP XAML hosting API in a C++ desktop (Win32) app](/windows/apps/desktop/modernize/using-the-xaml-hosting-api)