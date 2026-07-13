---
UID: NF:shobjidl.IUserNotificationCallback.OnContextMenu
title: IUserNotificationCallback::OnContextMenu (shobjidl.h)
description: Called when the user right-clicks (or presses SHIFT+F10) the icon in the notification area. The application should show its context menu in response.
helpviewer_keywords: ["IUserNotificationCallback interface [Windows Shell]","OnContextMenu method","IUserNotificationCallback.OnContextMenu","IUserNotificationCallback::OnContextMenu","OnContextMenu","OnContextMenu method [Windows Shell]","OnContextMenu method [Windows Shell]","IUserNotificationCallback interface","_shell_IUserNotificationCallback_OnContextMenu","shell.IUserNotificationCallback_OnContextMenu","shobjidl/IUserNotificationCallback::OnContextMenu"]
old-location: shell\IUserNotificationCallback_OnContextMenu.htm
tech.root: shell
ms.assetid: eb0b1de0-a42c-4789-aac0-885a574f89f6
ms.date: 12/05/2018
ms.keywords: IUserNotificationCallback interface [Windows Shell],OnContextMenu method, IUserNotificationCallback.OnContextMenu, IUserNotificationCallback::OnContextMenu, OnContextMenu, OnContextMenu method [Windows Shell], OnContextMenu method [Windows Shell],IUserNotificationCallback interface, _shell_IUserNotificationCallback_OnContextMenu, shell.IUserNotificationCallback_OnContextMenu, shobjidl/IUserNotificationCallback::OnContextMenu
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
ms.custom: 19H1
f1_keywords:
 - IUserNotificationCallback::OnContextMenu
 - shobjidl/IUserNotificationCallback::OnContextMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IUserNotificationCallback.OnContextMenu
---

# IUserNotificationCallback::OnContextMenu


## -description

Called when the user right-clicks (or presses SHIFT+F10) the icon in the notification area. The application should show its context menu in response.

## -parameters

### -param pt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

When returned by the method, takes a pointer to the <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure at the position of the mouse in the screen space where the click occurred.

In the case where user presses SHIFT+F10, the pointer points to the center of the icon in the screen space.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.