---
UID: NF:shobjidl.IUserNotificationCallback.OnBalloonUserClick
title: IUserNotificationCallback::OnBalloonUserClick (shobjidl.h)
description: Called when the user clicks the balloon. The application may respond with an action that is suitable for the balloon being clicked.
helpviewer_keywords: ["IUserNotificationCallback interface [Windows Shell]","OnBalloonUserClick method","IUserNotificationCallback.OnBalloonUserClick","IUserNotificationCallback::OnBalloonUserClick","OnBalloonUserClick","OnBalloonUserClick method [Windows Shell]","OnBalloonUserClick method [Windows Shell]","IUserNotificationCallback interface","_shell_IUserNotificationCallback_OnBalloonUserClick","shell.IUserNotificationCallback_OnBalloonUserClick","shobjidl/IUserNotificationCallback::OnBalloonUserClick"]
old-location: shell\IUserNotificationCallback_OnBalloonUserClick.htm
tech.root: shell
ms.assetid: b7360a2b-30ed-459e-ab6d-56a2127c2668
ms.date: 12/05/2018
ms.keywords: IUserNotificationCallback interface [Windows Shell],OnBalloonUserClick method, IUserNotificationCallback.OnBalloonUserClick, IUserNotificationCallback::OnBalloonUserClick, OnBalloonUserClick, OnBalloonUserClick method [Windows Shell], OnBalloonUserClick method [Windows Shell],IUserNotificationCallback interface, _shell_IUserNotificationCallback_OnBalloonUserClick, shell.IUserNotificationCallback_OnBalloonUserClick, shobjidl/IUserNotificationCallback::OnBalloonUserClick
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
 - IUserNotificationCallback::OnBalloonUserClick
 - shobjidl/IUserNotificationCallback::OnBalloonUserClick
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
 - IUserNotificationCallback.OnBalloonUserClick
---

# IUserNotificationCallback::OnBalloonUserClick


## -description

Called when the user clicks the balloon. The application may respond with an action that is suitable for the balloon being clicked.

## -parameters

### -param pt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

Takes a pointer to the <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure which, upon method return, points to the position of the mouse in screen space where the mouse click occurred.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.