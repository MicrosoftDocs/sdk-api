---
UID: NF:windows.ui.xaml.hosting.desktopwindowxamlsource.IDesktopWindowXamlSourceNative.get_WindowHandle
tech.root: winrt
title: IDesktopWindowXamlSourceNative::get_WindowHandle
ms.date: 07/25/2021
targetos: Windows
description: Gets the window handle of the parent UI element that is associated with the current IDesktopWindowXamlSourceNative instance.
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
 - IDesktopWindowXamlSourceNative::get_WindowHandle
f1_keywords:
 - IDesktopWindowXamlSourceNative::get_WindowHandle
 - windows.ui.xaml.hosting.desktopwindowxamlsource/IDesktopWindowXamlSourceNative::get_WindowHandle
dev_langs:
 - c++
---

## -description

Gets the window handle of the parent UI element that is associated with the current [IDesktopWindowXamlSourceNative](nn-windows-ui-xaml-hosting-desktopwindowxamlsource-idesktopwindowxamlsourcenative.md) instance.

## -parameters

### -param hWnd

On output, this parameter contains the window handle of the parent UI element that is associated with the current [IDesktopWindowXamlSourceNative](nn-windows-ui-xaml-hosting-desktopwindowxamlsource-idesktopwindowxamlsourcenative.md) instance.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an **HRESULT** error code.

## -remarks

## -see-also

[Using the UWP XAML hosting API in a C++ desktop (Win32) app](/windows/apps/desktop/modernize/using-the-xaml-hosting-api)