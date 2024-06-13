---
UID: NF:sharewindowcommandsourceinterop.IShareWindowCommandSourceInterop.GetForWindow
title: IShareWindowCommandSourceInterop::GetForWindow
description: Gets the [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource) object corresponding to a window identifier (a window handle). (IShareWindowCommandSourceInterop::GetForWindow)
prerelease: false
ms.date: 06/09/2021
tech.root: winrt
req.header: sharewindowcommandsourceinterop.h
req.include-header: 
req.construct-type: function
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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

> [!IMPORTANT]
> The **IShareWindowCommandSourceInterop::GetForWindow** API is part of a Limited Access Feature (see [LimitedAccessFeatures class](/uwp/api/windows.applicationmodel.limitedaccessfeatures)). For more information or to request an unlock token, contact [Microsoft Support](https://aka.ms/LAFAccessRequests).

## -parameters

### -param appWindow

Type: **[HWND](/windows/win32/winprog/windows-data-types)\***

The window identifier (a window handle) of the window where the call or meeting is established.

The window identified by the HWND passed in *appWindow* must be such that it is capable of providing the brand icon, and the friendly name, of the client application.

### -param riid

Type: **[REFIID](/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)**

A reference to the interface identifier of the **Windows::UI::Shell::IShareWindowCommandSource** interface.

### -param shareWindowCommandSource

Type: **[void](/windows/win32/winprog/windows-data-types)\*\***

The address of a **Windows::UI::Shell::IShareWindowCommandSource** pointer in which to receive the [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource) object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

For a code example, see [IShareWindowCommandSourceInterop](nn-sharewindowcommandsourceinterop-isharewindowcommandsourceinterop.md).

## -see-also

* [IShareWindowCommandSourceInterop](nn-sharewindowcommandsourceinterop-isharewindowcommandsourceinterop.md)

* [ShareWindowCommandSource](/uwp/api/windows.ui.shell.sharewindowcommandsource)
