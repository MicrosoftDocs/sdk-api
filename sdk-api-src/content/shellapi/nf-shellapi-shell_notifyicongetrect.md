---
UID: NF:shellapi.Shell_NotifyIconGetRect
title: Shell_NotifyIconGetRect function (shellapi.h)
description: Gets the screen coordinates of the bounding rectangle of a notification icon.
helpviewer_keywords: ["Shell_NotifyIconGetRect","Shell_NotifyIconGetRect function [Windows Shell]","_shell_Shell_NotifyIconGetRect","shell.Shell_NotifyIconGetRect","shellapi/Shell_NotifyIconGetRect"]
old-location: shell\Shell_NotifyIconGetRect.htm
tech.root: shell
ms.assetid: 81ad13be-a908-4079-b47c-6f983919700b
ms.date: 12/05/2018
ms.keywords: Shell_NotifyIconGetRect, Shell_NotifyIconGetRect function [Windows Shell], _shell_Shell_NotifyIconGetRect, shell.Shell_NotifyIconGetRect, shellapi/Shell_NotifyIconGetRect
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Shell_NotifyIconGetRect
 - shellapi/Shell_NotifyIconGetRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - Shell_NotifyIconGetRect
---

# Shell_NotifyIconGetRect function


## -description

Gets the screen coordinates of the bounding rectangle of a notification icon.

## -parameters

### -param identifier [in]

Type: <b>const <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyiconidentifier">NOTIFYICONIDENTIFIER</a>*</b>

Pointer to a <a href="/windows/desktop/api/shellapi/ns-shellapi-notifyiconidentifier">NOTIFYICONIDENTIFIER</a> structure that identifies the icon.

### -param iconLocation [out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that, when this function returns successfully, receives the coordinates of the icon.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/shell/notification-area">Notifications and the Notification Area</a>