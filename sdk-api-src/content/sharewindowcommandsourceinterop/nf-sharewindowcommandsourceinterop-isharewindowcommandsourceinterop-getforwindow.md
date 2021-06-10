---
UID: NF:sharewindowcommandsourceinterop.IShareWindowCommandSourceInterop.GetForWindow
title: IShareWindowCommandSourceInterop::GetForWindow
description: Gets the [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource) object corresponding to a window identifier (a window handle).
prerelease: true
ms.date: 06/09/2021
tech.root: winrt
req.header: sharewindowcommandsourceinterop.h
req.include-header: 
req.construct-type: function
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sharewindowcommandsourceinterop.h
api_name:
 - IShareWindowCommandSourceInterop::GetForWindow
f1_keywords:
 - IShareWindowCommandSourceInterop::GetForWindow
 - sharewindowcommandsourceinterop/IShareWindowCommandSourceInterop::GetForWindow
---

## -description

Gets the [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource) object corresponding to a window identifier (a window handle).

The window identifier represents the window where the call or meeting is established. This allows the Windows Shell to use the window identifier to obtain resources such as an icon, and to provide that as a hint to the user.

> [!NOTE]
> Thank you for your interest in consuming the **ShareWindowCommandSource** API within your application.
>
> The Windows Taskbar and associated user experience is a tightly controlled experience, used by millions of people around the world each day. This API is meant to be consumed by communications applications, and is a limited access feature.
>
> To request access, please email [onairapi@microsoft.com](mailto://onairapi@microsoft.com), and we will initiate your approval process.

## -parameters

### -param appWindow

### -param riid

### -param shareWindowCommandSource

## -returns

## -remarks

For a code example, see [IShareWindowCommandSourceInterop](nn-sharewindowcommandsourceinterop-isharewindowcommandsourceinterop.md).

## -see-also

* [IShareWindowCommandSourceInterop](nn-sharewindowcommandsourceinterop-isharewindowcommandsourceinterop.md)

* [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource)
