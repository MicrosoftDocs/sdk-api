---
UID: NF:winuser.SetProcessDpiAwarenessContext
title: SetProcessDpiAwarenessContext function (winuser.h)
description: Sets the current process to a specified dots per inch (dpi) awareness context. The DPI awareness contexts are from the DPI_AWARENESS_CONTEXT value.
helpviewer_keywords: ["SetProcessDpiAwarenessContext","SetProcessDpiAwarenessContext function [High DPI]","hidpi.setprocessdpiawarenesscontext","winuser/SetProcessDpiAwarenessContext"]
old-location: hidpi\setprocessdpiawarenesscontext.htm
tech.root: hidpi
ms.assetid: EACD1784-BEFF-46C1-8665-CBC86A65833C
ms.date: 12/05/2018
ms.keywords: SetProcessDpiAwarenessContext, SetProcessDpiAwarenessContext function [High DPI], hidpi.setprocessdpiawarenesscontext, winuser/SetProcessDpiAwarenessContext
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
 - SetProcessDpiAwarenessContext
 - winuser/SetProcessDpiAwarenessContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-dpi-l1-2-2.dll
 - User32.dll
api_name:
 - SetProcessDpiAwarenessContext
---

# SetProcessDpiAwarenessContext function


## -description

Sets the current process to a specified dots per inch (dpi) awareness context. The DPI awareness contexts are from the <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> value.

> [!NOTE]
> It is recommended that you set the process-default DPI awareness via application manifest, not an API call. See <a href="/windows/win32/hidpi/setting-the-default-dpi-awareness-for-a-process">Setting the default DPI awareness for a process</a> for more information. Setting the process-default DPI awareness via API call can lead to unexpected application behavior.

## -parameters

### -param value [in]

A <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> handle to set.

## -returns

This function returns TRUE if the operation was successful, and FALSE otherwise. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

Possible errors are <b>ERROR_INVALID_PARAMETER</b> for an invalid input, and <b>ERROR_ACCESS_DENIED</b> if the default API awareness mode for the process has already been set (via a previous API call or within the application manifest).

## -remarks

This API is a more advanced version of the previously existing <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness">SetProcessDpiAwareness</a> API, allowing for the process default to be set to the finer-grained <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> values. Most importantly, this allows you to programmatically set <b>Per Monitor v2</b> as the process default value, which is not possible with the previous API.

This method sets the default <a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a> for all threads within an application. Individual threads can have their DPI awareness changed from the default with the <a href="/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext">SetThreadDpiAwarenessContext</a> method.

You must call this API before you call any APIs that depend on the DPI awareness (including before creating any UI in your process). Once API awareness is set for an app, any future calls to this API will fail. This is true regardless of whether you set the DPI awareness in the manifest or by using this API.

If the DPI awareness level is not set, the default value is <b>DPI_AWARENESS_CONTEXT_UNAWARE</b>.

## -see-also

<a href="/windows/desktop/hidpi/dpi-awareness-context">DPI_AWARENESS_CONTEXT</a>

<a href="/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext">SetThreadDpiAwarenessContext</a>

<a href="/windows/win32/hidpi/setting-the-default-dpi-awareness-for-a-process">Setting the default DPI awareness for a process</a>
