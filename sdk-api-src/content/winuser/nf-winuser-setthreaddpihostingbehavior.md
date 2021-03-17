---
UID: NF:winuser.SetThreadDpiHostingBehavior
title: SetThreadDpiHostingBehavior function (winuser.h)
description: Sets the thread's DPI_HOSTING_BEHAVIOR. This behavior allows windows created in the thread to host child windows with a different DPI_AWARENESS_CONTEXT.
helpviewer_keywords: ["SetThreadDpiHostingBehavior","SetThreadDpiHostingBehavior function [High DPI]","hidpi.setthreaddpihostingbehavior","winuser/SetThreadDpiHostingBehavior"]
old-location: hidpi\setthreaddpihostingbehavior.htm
tech.root: hidpi
ms.assetid: CF31D96A-EC84-4911-81A2-82EC90D417B9
ms.date: 12/05/2018
ms.keywords: SetThreadDpiHostingBehavior, SetThreadDpiHostingBehavior function [High DPI], hidpi.setthreaddpihostingbehavior, winuser/SetThreadDpiHostingBehavior
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadDpiHostingBehavior
 - winuser/SetThreadDpiHostingBehavior
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - SetThreadDpiHostingBehavior
---

# SetThreadDpiHostingBehavior function


## -description

Sets the thread's <a href="/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a>. This behavior allows windows created in the thread to host child windows with a different <b>DPI_AWARENESS_CONTEXT</b>.

## -parameters

### -param value

The new <a href="/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> value for the current thread.

## -returns

The previous <a href="/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> for the thread. If the hosting behavior passed in is invalid, the thread will not be updated and the return value will be <b>DPI_HOSTING_BEHAVIOR_INVALID</b>. You can use this value to restore the old <b>DPI_HOSTING_BEHAVIOR</b> after overriding it with a predefined value.

## -remarks

<a href="/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a> enables a mixed content hosting behavior, which allows parent windows created in the thread to host child windows with a different <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> value. This property only effects new windows created within this thread while the mixed hosting behavior is active. A parent window with this hosting behavior is able to host child windows with different <b>DPI_AWARENESS_CONTEXT</b> values, regardless of whether the child windows have mixed hosting behavior enabled.

This hosting behavior does not allow for windows with per-monitor <b>DPI_AWARENESS_CONTEXT</b> values to be hosted until windows with <b>DPI_AWARENESS_CONTEXT</b> values of system or unaware.

To avoid unexpected outcomes, a thread's <b>DPI_HOSTING_BEHAVIOR</b> should be changed to support mixed hosting behaviors only when creating a new window which needs to support those behaviors. Once that window is created, the hosting behavior should be switched back to its default value.

This API is used to change the thread's <b>DPI_HOSTING_BEHAVIOR</b> from its default value. This is only necessary if your app needs to host child windows from plugins and third-party components that do not support per-monitor-aware context. This is most likely to occur if you are updating complex applications to support per-monitor  <b>DPI_AWARENESS_CONTEXT</b> behaviors.

Enabling mixed hosting behavior will not automatically adjust the thread's <b>DPI_AWARENESS_CONTEXT</b> to be compatible with legacy content. The thread's awareness context must still be manually changed before new windows are created to host such content.

## -see-also

<a href="/windows/desktop/api/windef/ne-windef-dpi_hosting_behavior">DPI_HOSTING_BEHAVIOR</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior">GetThreadDpiHostingBehavior</a>



<a href="/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior">GetWindowDpiHostingBehavior</a>