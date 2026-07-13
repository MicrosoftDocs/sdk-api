---
UID: NF:shellscalingapi.RegisterScaleChangeNotifications
title: RegisterScaleChangeNotifications function (shellscalingapi.h)
description: Registers a window to receive callbacks when scaling information changes.
helpviewer_keywords: ["RegisterScaleChangeNotifications","RegisterScaleChangeNotifications function [Windows Shell]","shell.RegisterScaleChangeNotifications","shellscalingapi/RegisterScaleChangeNotifications"]
old-location: shell\RegisterScaleChangeNotifications.htm
tech.root: shell
ms.assetid: 79FB0A54-EBF0-4aab-B631-B4D3EA54D20B
ms.date: 12/05/2018
ms.keywords: RegisterScaleChangeNotifications, RegisterScaleChangeNotifications function [Windows Shell], shell.RegisterScaleChangeNotifications, shellscalingapi/RegisterScaleChangeNotifications
req.header: shellscalingapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OneCore.Lib
req.dll: Shcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterScaleChangeNotifications
 - shellscalingapi/RegisterScaleChangeNotifications
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shcore.dll
 - API-MS-Win-shcore-scaling-l1-1-0.dll
 - API-MS-Win-shcore-scaling-l1-1-1.dll
 - API-MS-Win-ShCore-Scaling-l1-1-2.dll
 - api-ms-win-shcore-scaling-l1.dll
api_name:
 - RegisterScaleChangeNotifications
---

# RegisterScaleChangeNotifications function


## -description

Registers a window to receive callbacks when scaling information changes.
<div class="alert"><b>Note</b>  This function is not supported as of Windows 8.1. Use <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangeevent">RegisterScaleChangeEvent</a> instead.</div><div> </div>

## -parameters

### -param displayDevice [in]

Type: <b><a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-display_device_type">DISPLAY_DEVICE_TYPE</a></b>

The enum value that indicates which display device to receive notifications about.

### -param hwndNotify [in]

Type: <b>HWND</b>

The handle of the window that will receive the notifications.

### -param uMsgNotify [in]

Type: <b>UINT</b>

An application-defined message that is passed to the window specified by <i>hwndNotify</i> when scaling information changes.  Typically, this should be set to <a href="/windows/desktop/winmsg/wm-app">WM_APP</a>+<i>x</i>, where <i>x</i> is an integer value.

### -param pdwCookie [out]

Type: <b>DWORD*</b>

Pointer to a value that, when this function returns successfully, receives a registration token. This token is used to revoke notifications by calling <a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-revokescalechangenotifications">RevokeScaleChangeNotifications</a>.

## -returns

Type: <b>STDAPI</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This message specified by <i>uMsgNotify</i> is posted to the registered window through <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a>. The <i>wParam</i> of the message can contain a combination of <a href="/windows/desktop/api/shellscalingapi/ne-shellscalingapi-scale_change_flags">SCALE_CHANGE_FLAGS</a> that describe  the change that occurred.

## -see-also

<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-getscalefactorformonitor">GetScaleFactorForMonitor</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-registerscalechangeevent">RegisterScaleChangeEvent</a>



<a href="/windows/desktop/api/shellscalingapi/nf-shellscalingapi-unregisterscalechangeevent">UnregisterScaleChangeEvent</a>