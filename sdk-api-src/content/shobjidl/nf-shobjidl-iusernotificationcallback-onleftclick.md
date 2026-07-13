---
UID: NF:shobjidl.IUserNotificationCallback.OnLeftClick
title: IUserNotificationCallback::OnLeftClick (shobjidl.h)
description: Called when the user clicks the icon in the notification area. The applications may launch some customary UI in response.
helpviewer_keywords: ["IUserNotificationCallback interface [Windows Shell]","OnLeftClick method","IUserNotificationCallback.OnLeftClick","IUserNotificationCallback::OnLeftClick","OnLeftClick","OnLeftClick method [Windows Shell]","OnLeftClick method [Windows Shell]","IUserNotificationCallback interface","_shell_IUserNotificationCallback_OnLeftClick","shell.IUserNotificationCallback_OnLeftClick","shobjidl/IUserNotificationCallback::OnLeftClick"]
old-location: shell\IUserNotificationCallback_OnLeftClick.htm
tech.root: shell
ms.assetid: 0202aace-94d6-4619-8838-eea0b174ffb6
ms.date: 12/05/2018
ms.keywords: IUserNotificationCallback interface [Windows Shell],OnLeftClick method, IUserNotificationCallback.OnLeftClick, IUserNotificationCallback::OnLeftClick, OnLeftClick, OnLeftClick method [Windows Shell], OnLeftClick method [Windows Shell],IUserNotificationCallback interface, _shell_IUserNotificationCallback_OnLeftClick, shell.IUserNotificationCallback_OnLeftClick, shobjidl/IUserNotificationCallback::OnLeftClick
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
 - IUserNotificationCallback::OnLeftClick
 - shobjidl/IUserNotificationCallback::OnLeftClick
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
 - IUserNotificationCallback.OnLeftClick
---

# IUserNotificationCallback::OnLeftClick


## -description

Called when the user clicks the icon in the notification area. The applications may launch some customary UI in response.

## -parameters

### -param pt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

Takes a pointer to the <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure which, when the method returns, points to the position of the mouse in the screen space where the mouse click occurred.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.