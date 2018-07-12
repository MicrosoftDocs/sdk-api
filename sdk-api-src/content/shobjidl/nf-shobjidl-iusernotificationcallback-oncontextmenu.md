---
UID: NF:shobjidl.IUserNotificationCallback.OnContextMenu
title: IUserNotificationCallback::OnContextMenu
author: windows-sdk-content
description: Called when the user right-clicks (or presses SHIFT+F10) the icon in the notification area. The application should show its context menu in response.
old-location: shell\IUserNotificationCallback_OnContextMenu.htm
old-project: shell
ms.assetid: eb0b1de0-a42c-4789-aac0-885a574f89f6
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IUserNotificationCallback interface [Windows Shell],OnContextMenu method, IUserNotificationCallback.OnContextMenu, IUserNotificationCallback::OnContextMenu, OnContextMenu, OnContextMenu method [Windows Shell], OnContextMenu method [Windows Shell],IUserNotificationCallback interface, _shell_IUserNotificationCallback_OnContextMenu, shell.IUserNotificationCallback_OnContextMenu, shobjidl/IUserNotificationCallback::OnContextMenu
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IUserNotificationCallback.OnContextMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IUserNotificationCallback::OnContextMenu


## -description


Called when the user right-clicks (or presses SHIFT+F10) the icon in the notification area. The application should show its context menu in response.



## -parameters




### -param pt [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>*</b>

When returned by the method, takes a pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure at the position of the mouse in the screen space where the click occurred.

In the case where user presses SHIFT+F10, the pointer points to the center of the icon in the screen space.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



